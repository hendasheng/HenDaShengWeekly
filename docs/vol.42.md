# 很大声周刊-vol.42
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![image](https://user-images.githubusercontent.com/20842136/155922406-f6cebac8-ea83-4151-a353-710af6d04ab9.png)

# 孔雀计划：中文字体排印的思路 - The Type
![image](https://user-images.githubusercontent.com/20842136/155922543-a68a3396-b71a-4239-b992-535556379316.png)

> 孔雀计划：中文字体排印的思路」由本站作者 [Eric Liu](https://www.thetype.com/author/ericliu/) 于 2017 年发起，系列倡导从中文出发、以中文的思维方式讨论中文排版。

# 字谈字畅
![image](https://user-images.githubusercontent.com/20842136/155922784-f38824fd-575b-44bd-978d-12cb11c35eef.png)

《字谈字畅》（TypeChat）是全球首家用华语制作的字体排印主题播客节目，由 [The Type](https://www.thetype.com/typechat/) 出品，于 2015 年 9 月正式开播上线。

# Generative Art Studio
![image](https://user-images.githubusercontent.com/20842136/155922933-d5a05b02-9aa7-4b15-b81e-ea3033a4da0a.png)

> CG艺术家1993年1月29日来自东京
> 为雅虎工作！ 日本和亚马逊日本（网页设计师）。 目前是一名自由CG艺术家。 负责日本最大的音乐节 ROCK IN JAPAN FESTIVAL 和 COUNTDOWN JAPAN 的 CG 视频。 我曾获得许多奖项“亚洲数字艺术奖”、CSS 设计奖“SPECIAL KUDOS”、亚洲设计奖“今日设计”等。在日本和海外的展览。在星巴克举办了 3CG 个展。国际艺术博览会， SICF, Shanghai ART BOOK FAIR. 入选日本动态图形创作者 100 强。

![image](https://user-images.githubusercontent.com/20842136/155924331-666b645b-1446-42f9-9239-715744a37b75.png)

![image](https://user-images.githubusercontent.com/20842136/155924360-4c78d20c-27ef-46ef-9e39-cec85a4148e4.png)

[玉澤芽衣 - Generative Art Studio](https://generativeartstudio.tokyo/about/) 我发现学习新技术很有趣，而且我正在做一个像肌肉训练这样的项目，每天都会产生艺术。

# [Blender] 初心者のためのGeometry Nodes入門
![image](https://user-images.githubusercontent.com/20842136/155924937-a3c15e13-6853-4c32-8271-9eb031ccf193.png)

作者 [Junichiro Horikawa](https://twitter.com/jhorikawa_err) 是一位建筑设计师，通过 Houdini 算法进行设计，同时也搭配 Unity 工作，最近开始研究 Blender，并录制了这条 [Blender 几何节点入门教程](https://www.youtube.com/watch?v=yQgfsVy62Sw&t=6s)，研究能力和学习速度让人羡慕。

# Blender 通过命令行渲染多个文件
Blender 软件中没有批量渲染的功能，遇到批量渲染需求时很头疼，最近发现可以通过命令行的方式解决。

![image](https://user-images.githubusercontent.com/20842136/155923261-5520ee27-0869-4d92-8bfe-5db73dc213cd.png)

1. 在 Blender 安装目录中右键，选择通过终端打开。

![image](https://user-images.githubusercontent.com/20842136/155923292-53a2d401-586e-4b36-aa44-d0e3c8084700.png)

2. 此时命令行会显示为 `C:\Program Files\Blender Foundation\Blender 3.0`，你的可能有所不同，区别在于最后的 Blender 版本号。

![image](https://user-images.githubusercontent.com/20842136/155923322-df489135-b177-4b65-b1d5-89114c1e56ae.png)

3. 找到需要渲染的文件，在 blender 中设置好输出地址，右键选择「复制文件地址」。
4. 回到命令行，输入 `blender -b filename.blend -f 1`，这条命令的意思是渲染这个文件的第一帧（`-f 1`），第十帧则是（`-f 10`），这时程序会自动渲染结果；`blender -b filename.blend -a` 代表输出整个动画。还有更多命令操作方式，搭配 [如何连续批量渲染多个混合文件？](https://qa.1r1g.cn/blender/ask/5232531/)、[命令行渲染](https://docs.blender.org/manual/zh-hans/latest/advanced/command_line/render.html) 服用效果更佳。