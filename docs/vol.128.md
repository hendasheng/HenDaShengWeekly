# 很大声周刊-vol.128
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![img](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3f290073-8def-43cf-a62b-868cba407cfa)

# 视频转 Hap 编码 - 批量处理（Python + FFmpeg)

## 为什么用 Hap 编解码器？
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d49e624b-cb46-42a9-a719-a4c77edb35cc)

> [Hap](https://hap.video/using-hap) 是一组适用于 macOS、Windows 和 Linux 的视频编解码器，它使用计算机的图形硬件执行解压缩，从而大大减少播放视频所需的 CPU 使用率。它已成为媒体服务器上高性能、高分辨率电影播放、实时视频性能和活动视觉效果的标准。

可以简单理解为针对实时视频的编解码方案，减少 CPU 使用率，通过 GPU 硬件加速解码，避免卡顿。

我尝试加载 300 个视频随机抽取播放、跳转，常规 H264 编码格式会在过程中出现卡顿，转成 HAP 编码后流畅到让人感动。

## 视频转 Hap 编码 - 批量处理（Python + FFmpeg)
![ezgif com-video-to-gif (6)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/af0da96e-eb04-44ed-85c2-8c3078a56648)

前提：
- 了解基本的 Python 语法
- 安装 [FFmpeg](https://ffmpeg.org/download.html:blank)
- [源码 - videosToHapCodecs.py](https://gist.github.com/hendasheng/8ef9383732368dacf89898505832fb25)

用到 [subprocess](https://docs.python.org/zh-cn/3/library/subprocess.html)、[os](https://docs.python.org/zh-cn/3/library/os.html) 两个模块，分别用于执行命令和读写文件。

主要有三个方法：

- **`createFloder()`**
在当前目录创建新文件夹，并检测是否已有，重复则跳过。
``` python
def createFolder():
    subDirectory = "Hap_Codecs"
    savePath = os.path.join(inputPath, subDirectory)
    try:
        os.mkdir(savePath)
        print(f"已创建文件夹: {savePath}")
    except FileExistsError:
        print(f"文件夹已存在: {savePath}")
    return savePath
```

- **`loopFile(path)`**
读取文件夹中的内容，并过滤掉文件夹和非视频格式的文件。
``` python
def loopFile(path):
    count = 0
    for root, dirs, files in os.walk(path):
        dirs.clear() # 不读取子目录
        for i in files:
            if i.lower().endswith(('.mp4', '.avi', '.mkv', '.mov')):  # 只读取视频文件
                file_path = os.path.join(root, i)
                file_name = os.path.splitext(i)[0]
                yield file_path, file_name
                count += 1
                # print(file_name)
    print("已将 {} 个视频文件进行 HAP 转码处理".format(count))
```
- **`main()`**
对每个文件执行编码转换命令（通过 FFmpeg），并保存到输出文件夹中。
ffmpeg 转 HAP 编码命令： `ffmpeg -i input.mov -c:v hap output.mov`
``` python
def main():
    savePath = createFolder()
    for index, value in enumerate(loopFile(targetPath)):
        file_path = value[0]
        file_name = value[1]
        outPath = os.path.join(savePath, file_name + "_hap.mov")
        subprocess.run(["ffmpeg", "-i", file_path, "-c:v", "hap", outPath], shell = True)
```
搭配 ChatGTP 服用效果更佳。

# Touchdesigner 中的两种引用方式
## op() 引用
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/889dd51b-5784-48fc-b386-e9000cdc8cd1)

`len(op('switch2').inputs)`

获取「switch2」节点的输入总数。

## python
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/99ed46c7-7d31-4f66-8ccd-4a79acfd3f69)

通过 python 获取相应值。
``` python
top_switch = op('switch2')
inputCount = len(top_switch.inputs)

print(inputCount)
```
再通过 mod() 方法引用。
`mod('text_getSwitch_Len').inputCount`


引用非常重要，尽可能减少手动填写值可以极大提高整体可控性。在对处理变量时，比如获取一个随机游走小球的位置，也只能通过引用完成，引用真好。

# Houdini 中的通过 vex 获取值
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0c6fed8b-4381-40b3-9861-173ccd3a0248)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/fe784dce-8397-4f7e-a0a3-b41f4f8fe499)

``` C++
// 获取点位置信息
vector pos1 = point(0, "P", 0);
vector pos2 = point(0, "P", 1);

// 提取 x 轴位置
float p1 = pos1.x;
float p2 = pos2.x;

// 将结果转换为字符串
s@str_p1 = sprintf("%5.5f", p1);
s@str_p2 = sprintf("%5.5f", p2);

```
[sprintf - 将结果转换为字符串](https://www.sidefx.com/docs/houdini/vex/functions/sprintf.html)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/9cc1b11d-ac39-41f3-a9ee-c9bdc2541956)

# 小白兔白又白
![微信图片_20231021170154](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/fa33c63b-3081-4654-9792-7db816c6005a)
![微信图片_20231021170151](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/e20b32c9-64fa-4213-99e3-2c1a9068f36e)
![微信图片_20231021165441](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ee958e42-4af9-4f4e-a05b-2069651e5b3e)

# We Are All Insane - AWOLNATION
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/552d040a-6ccd-493c-9dc6-c8d184534220)
