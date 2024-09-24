# 很大声周刊-vol.150
![Title_WeChat_150](https://github.com/user-attachments/assets/eee6d8f4-ec6a-4b37-877a-e1bfa654ddbc)

# 在离线渲染中实现节奏控制

稍微有点绕，先说实时渲染的节奏控制，这个很好理解，节奏和画面渲染都是实时运行的，所以在时间上是完全同步的，节奏发出的信号会同步体现在渲染画面中。

离线渲染就不是这么回事了，离线渲染的特性就是通过更长的渲染时间换取更高质量的渲染结果，这种情况下节奏发出的信号不能同步反应在渲染结果中。

其实也很简单，最常用的关键帧就是在解决这个问题，可是关键帧实现节奏控制很麻烦、调试成本也很高，我想能不能通过更自动化方式完成这件事。

Houdini 在这方面做的很好，除了用已有的模块外，还可以直接在节点中嵌入代码，更准确地实现自己的需求，这是最近的一项测试。

![693_StringArray_Index-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/2462c2ad-88a1-4661-8b4e-ae1dbac58ac2)

![image](https://github.com/user-attachments/assets/92e8c5fa-1252-40fc-8cf8-2384ad07d772)

``` C++
string strs[] = {"123", "abc", "!@#"};

if (@Frame % 10 == 1) @index ++;

@index = @index % len(strs); // 如果超出长度则循环回第一个元素
s@str = strs[i@index]; // 选择当前索引的字符串
```

类似需求实现起来很方便，所以这个尝试也就用 Houdini 来实现了。

![2024-09-2501 54 33-ezgif com-optimize](https://github.com/user-attachments/assets/b49ed0f3-5838-4e44-b8e7-07dbb42b9a39)

关键帧和节奏都是时间概念，既然都是时间概念，那应该就能互相转换，就像分、秒，米、厘米一样能互相转换。这东西有点复杂，我只是尽量把问题描述清楚，交给 ChatGTP，经过几轮调试果然得到了不错的答案。

``` C++
int frames_per_beat = 15;  // 每拍 15 帧
float frames_per_32_note = frames_per_beat / 8.0;  // 每个 32分音符对应的帧数

// 定义音符触发的音符编号（0, 8, 16, 19, 23）
int note_intervals[] = {0, 8, 16, 24};  
int frame_intervals[];  // 用于存储计算出来的帧数

// 计算音符对应的帧数
for (int i = 0; i < len(note_intervals); i++) {
    frame_intervals[i] = int(rint(note_intervals[i] * frames_per_32_note));  // 计算并四舍五入
}

// 当前帧，限定在 0 到 59 帧范围内
int current_frame = int(@Frame % 60);

// 只在 0 到 59 帧范围内进行触发判断
if (current_frame < 60) {
    foreach(int frame; frame_intervals) {
        if (current_frame == frame + 2) {
            @count += 1;
        }
    }
}
```

当前的代码中的 `@count` 控制模型形态变化，也就是通过节奏控制 `@count` 的值，由它驱动模型变化，画面中的粒子也是同样的原理，声音包含底鼓和踩镲，分别驱动模型变换和粒子发射，踩镲节奏更为密集，所以画面中粒子的动态也会更频繁。

原理就是各种转换，现在只要写好在第几个音符上触发，程序会自动转换成关键帧动画，调试只需要更改音符就好。

它需要你对代码、节奏有一定的了解，没啥硬性要求，代码部分的底线是能看懂它在干什么，节奏部分的底线是知道如何描述需求。比如，120 BPM 1 / 32（每分钟 120 拍的速度，每拍 32 个音符），我需要在第 1、9、17、25 个音符触发等等。

还有节奏部分依然用到 [MaxMsp](https://cycling74.com/products/max)，最近用它做各种控制器，可太方便了。

如果你也遇到类似需求，或者就想做一些奇怪的尝试，希望这对你有帮助。

# Houdini 安装 MOPs（Mac）

![img](https://github.com/user-attachments/assets/70bf8252-d316-4a91-80b9-50b381560ec6)

[Mops](https://www.motionoperators.com/) 几乎是 Houdini 不可缺少的插件，开源且强劲。Windows 端安装非常简单，Mac 上面会出现一些关于安装路径的问题，我在论坛中（[Mac M3 Houdini 安装 Mops 无效](https://www.sidefx.com/forum/topic/97703/) ）记录了遇到的问题，以及解决方法。

# Birthday Resistance Parade - World's End Girlfriend
![image](https://github.com/user-attachments/assets/2511d48a-d746-46a5-b8dd-ef2e7b7b5c3e)
