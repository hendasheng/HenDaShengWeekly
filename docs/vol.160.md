# 很大声周刊-vol.160 | Kimi K2 Thinking × P5js 实时 MIDI 渲染

最近在探索 MIDI 可视化的相关内容，想做一个根据 MIDI 输入实时显示视觉效果的工具，正巧 kimi 发布了新模型 [Kimi K2 Thinking](https://mp.weixin.qq.com/s/oQp1kFpoYFhYQ8GzbwZLyA?from=groupmessage&isappinstalled=0&scene=1&clicktime=1762614289&enterid=1762614289)，是 Kimi 迄今能力最强的开源思考模型。正好在实际项目中体验一下。

初步的想法来源于 Ableton Live 和 Ableton Move，它们是我常用的音乐工具。

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-09_22-41-10.png)

我想 MIDI 输入的视觉效果就像 Ableton Live 中的音轨那样，音符横向排列。

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-09_22-45-01.png)

窗口中肯定不能只有一轨，这样太单调了，所以就像 Ableton Move 那样，有四个轨道，起码能容纳一首歌基本的器乐配置。

其它部分并没有很详细的打算，边做边看，以下简单记录了整个过程，使用 Tare + Kimi K2 Thinking 实现。

### 基本功能测试

> 帮我创建一个 midi 接收功能

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-08_21-44-58.png)


### 实现音轨功能 / 样式

> 帮我创建一个 class，把它想象成一条音轨，用来接收 midi，midi 值用圆点表示，值越低 y 轴越低，横向依次排列

> 很好，增加一条时间线，在最新 midi 的最右端，另外在增加格子，整个轨道想象成钢琴卷帘那种

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-08_22-12-38.png)

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-08_22-10-54.png)


### 多个音轨

> 我想纵向多个音轨，比如 2 个，每个音轨在传参中设置通道值，这样就互相不影响了

> 我希望在轨道左侧显示一些基本信息，比如通道值，轨道编号

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-08_23-16-09.png)

### 调整背景网格，增加控制菜单

>增加 tweakpane 菜单，控制是否显示轨道左侧的文字注释
>
>现在背景格子逻辑没问题，但是观感不好，帮我把格子换成矩阵点，不需要这么密集

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-08_23-24-33.png)

### 丰富音轨
>轨道增加不同的形状比如 1 2 3，在传参中通过编号控制当前轨道显示那种形状

> 传参中增加色值，"ffbe86-ffe156-ffe9ce-ffb5c2-3777ff", block 中自动提取颜色，新增 midi 元素随机选择色值，已有的不要变啊，时间线颜色为色值的第一个

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-09_00-33-34.png)

### 增加控制菜单
> 增加菜单
> 轨道控制 -> 色值 / 尺寸 / 样式
> 控制像跟随轨道数量，每个选项分别控制对应轨道

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-10_15-06-59.png)

> midi 文字这部分，能否引入可变字体，字体样式的粗细从 透明度映射

> 全局控制菜单加一项，显示 FPS

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-10_15-17-31.png)

---

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-09_22-54-49.png)

以上是整个过程中关键步骤的记录，中间有很多调整、尝试，甚至彻底推翻一些想法，Kimi 提供了很好的支持，如果留意过程截图中的模型型号，会发现从最开始的用到的是 kimi-k2-thinking-turbo，也就是最强的版本，切换到了 kimi-k2-turbo-preview。

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-10_15-12-29.png)

原因很简单，turbo / preview 两个版本可以简单理解为前者超级强力，但需要更多思考时间，后者则是更轻量的版本，但速度更快。preview 既能满足我的需求，也有着很好的速度。

最后，AI 极大拓展了我们的活动半径，很多以前做不到的事情，现在都可以尝试，但话说回来，AI 本身的能力是一回事，怎么使用它是另一回事。创作者对于所作事情的了解程度会直接影像 AI 的发挥，它需要根据你的问题给出结果，这让我想到了一篇文章 [《提问的智慧》](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/main/README-zh_CN.md)。

> 在黑客的世界里，你所提技术问题的解答的好坏, 很大程度上取决于你提问的方式与此问题的难度。本指南将教你如何正确地提问以获得你满意的答案。
> -- 《提问的智慧》

在以前这是面向开发者的文章，帮助你正确地提问以获得你满意的答案，我想在当下这并不过时，所有人都可以尝试通过 AI 工具实现自己的想法，所有人都需要更好地提问，从而更高效的获得解决方案（和人类的精力一样，AI 的使用额度也是有限的）。