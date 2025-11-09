# 很大声周刊-vol.160 |  Kimi K2 Thinking - MIDI

我尝试搭建基于 p5js 的 midi 可视化工具，正巧 kimi 发布了新的模型 Kimi K2 Thinking


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

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-09_00-55-07.png)

> midi 文字这部分，能否引入可变字体，字体样式的粗细从 透明度映射

> 全局控制菜单加一项，显示 FPS

![](https://picgo-mdeia.oss-cn-beijing.aliyuncs.com/picgo/midi_visual/Snipaste_2025-11-09_01-24-16.png)


在你对你所做的事情有足够了解时，会显得 AI 更聪明。