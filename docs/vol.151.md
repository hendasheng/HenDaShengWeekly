# 很大声周刊-vol.151

# OSC、MIDI 信号收发方案
- [TouchOSC](https://hexler.net/touchosc)
    基于应用程序的信号收发产品，移动、桌面端都有很好的支持；
- [Open Stage Control](https://openstagecontrol.ammd.net/)
    基于浏览器的信号收发；
- [MaxMsp](https://cycling74.com/)
    MaxMsp 是艺术家和创意人士探索音乐、视觉和技术极限的重要平台，收发信号只是其中的一小部分功能，在这里可以实现更复杂的信号处理；
- [Ableton Live](https://www.ableton.com/)
    Ableton Live 本身是做音乐的软件，它更偏向即兴创作和现场表演，最重要的是 [Max for Live](https://www.ableton.com/zh-cn/live/max-for-live/) 模块，它的主要作用就是通过 Max 实现自定义功能，连接、控制外部软硬件实现更好玩的效果，OSC、MIDI 信号是众多连接方式中的一种；
    - [LiveGrabber](https://support.showsync.com/sync-tools/livegrabber/introduction) - [LiveGrabber 在 Ableton Live 中发送/接收 OSC](https://sonicbloom.net/livegrabber-to-sendreceive-osc-in-ableton-live/)；

---
它们本身都是很好的工具，在不同场景下根据需求选择即可。

强烈建议大家去看下 [Max 的介绍页面](https://cycling74.com/products/max8)，大概率不能完全看懂，不过能知道它大概可以干嘛，或者了解能不能通过它实现自己的想法。

我用到的组合是 MaxMsp 和 Ableton Live，因为多数情况下会有声音参与，这也是我探索的方向。它们两个关系非常紧密，MaxMsp 一定程度上也可以被当作音乐工具，只是对我来说有点复杂，我基本只用它制作信号，在 Ableton Live 中完成声音处理。

上面提到的工具都是收/发信号的工具，当前语境下更多用于发送信号，接下来要聊的是向哪里发送信号。

OSC 的逻辑是保证收发两端处在相同的 IP 地址（IP Address）和端口（Port），这时已经建立通讯，接下来由发送端发送信号（Message Address），在接收端把信号映射到控制项上就完成了整个过程。

各家工具会有用法差异，但逻辑完全相同，以 Blender 和 Unreal 为例：

**Blender**
![20241006-165307-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/a3f14813-04ce-4b0f-a7a3-3ff1a0cf63f5)

![image](https://github.com/user-attachments/assets/cdea6b4d-fbcc-4295-aff2-f90236fa3457)

Blender 会用到 [NodeOSC](https://github.com/maybites/NodeOSC?tab=readme-ov-file)，发送端以一定频率随机发送两组字符串，Blender 接收到信号并保存到字符串节点中，最终显示在画面上。

这么描述太抽象，文件会放在 [GitHub 仓库中](https://github.com/hendasheng/HenDaShengWeekly) `data\vol_155`，看起来会更直观，整个过程很简单。

**Unreal**
![image](https://github.com/user-attachments/assets/69d7a39c-ab7f-40b4-8e9e-966214874507)

Unreal 相对复杂，但同时也带来更丰富的控制，建立 OSC 通讯是第一步，[Open Stage Control with Unreal 5.1 (Tutorial)](https://www.youtube.com/watch?v=42eDMmvokMM&t=832s)，这份教程解决了我在 OSC 上遇到的大部分问题，问题有很多种解决方法，这位作者的方法简洁又聪明。

---

![Render_01 0140](https://github.com/user-attachments/assets/15a2bd41-8682-4e15-a69c-b8fef9b12ec9)

![image](https://github.com/user-attachments/assets/25327977-a467-47f0-9da1-43eb7fbec75e)

最近开发片段中的 OSC 控制都是通过这种方法完成，Ableton Live 向 Max 发送 MIDI 信号，经过 Max 处理后，向 Unreal 发送 OSC 信号，实现实时控制。

中间还用到一些很方便的工具：
- [Create Volumetric Cloud Inside Unreal Engine 5](https://www.youtube.com/watch?v=3nH7VyBwBNA) - VDB 云；
- [The Secret to Photoreal Skies in Unreal Engine](https://www.youtube.com/watch?v=Yq1Y2FWj5aQ&t=144s) - HDRIBackdrop 天空环境；
- [如何将影片渲染队列用于高质量渲染 Unreal](https://dev.epicgames.com/documentation/zh-cn/unreal-engine/rendering-high-quality-frames-with-movie-render-queue-in-unreal-engine) - 配置控制台变量；

整个过程没有完整的教程，感兴趣的朋友可以按图索骥，每一步都不难，正好可以结合自身需求实现自己的想法。

# J74 HarmoTools - 和弦可视化
![image](https://github.com/user-attachments/assets/55b3c3ec-4655-4627-a62c-6b74fa23b759)

> [J74 HarmoTools](https://fabriziopoce.com/HarmoTools.html) 是一组用于实时 MIDI 和声的设备，通过跟随领先 MIDI 轨道的和弦和/或音阶来调整多个 MIDI 轨道。该工具提供了用于 MIDI 分析、可视化、过滤以及创建的构建块。还包括用于网络协作的工具。用于现场演出，最终使用 TCP/IP 网络与其他音乐家合作。

![image](https://github.com/user-attachments/assets/dec273b5-fe72-4def-903a-e34f8768e22c)

好像有很多功能，我只会用显示和弦，光是这一点就很够用，很多时候我都不知道自己在按啥。

# CG 电影摄影 - Christophe Brejon
![image](https://github.com/user-attachments/assets/63242659-1f8e-456f-9ba7-4ae51db12d69)

[CG 电影摄影](https://chrisbrejon.com/)

# 小白兔白又白
![微信图片_20241006175450](https://github.com/user-attachments/assets/b4ad60a1-f04a-42f0-b04a-78bcdfc028e2)
![微信图片_20241006175445](https://github.com/user-attachments/assets/570b68d0-edf6-4f66-8ff7-2a0b4cc1dfc7)

# Martin - Ben Böhmer
![image](https://github.com/user-attachments/assets/bdb71914-1f57-4a93-8114-e8c3959bb3c9)
