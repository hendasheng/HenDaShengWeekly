# 很大声周刊-vol.78
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_78](https://user-images.githubusercontent.com/20842136/200114354-8249d48c-4785-4925-9fce-1275eee3e23a.png)

# 传递属性 - Houdini
![image](https://user-images.githubusercontent.com/20842136/200115879-3a50d52b-8182-4b7d-b1e8-229dc9e438bf.png)

[传递属性 ](https://www.sidefx.com/docs/houdini/nodes/sop/attribtransfer.html) 看起来字面意思很清楚，可是我一直搞不清楚具体用途，最近有了一点点进展。

「属性」在操作过程中并不会永久保存，有时候是根据需要被手动清理掉，还有些时候是操作本身会自动清理掉当前属性。

![image](https://user-images.githubusercontent.com/20842136/200116313-8b599d80-6ab1-4744-9657-04b415dc5afc.png)

比如 VDB，在做 VDB 处理前除了位置属性外还有很多其它属性。

![image](https://user-images.githubusercontent.com/20842136/200116291-378819eb-04eb-48b7-9f16-9897841a6a1c.png)

在经过 VDB 处理后就只剩位置属性了。

![image](https://user-images.githubusercontent.com/20842136/200116407-26623149-789e-4367-8b2f-da533779ffc5.png)

如果此刻我想用之前的 「curveu」属性为物体设置颜色，这个属性的作用是记录曲线的两个端点，用它可以实现曲线渐变色。可是经过 VDB 处理后，这个属性已经没有了。

![image](https://user-images.githubusercontent.com/20842136/200116566-a2afd1f5-6d28-4f3e-931e-1160113aa650.png)

这种情况下就需要把 VDB 处理前的 「curveu」属性，通过「传递属性」拿过来，这样就即做到 VDB 处理，又没丢失需要的属性。

「传递属性」真好。

# Snapdrop 基于浏览器的本地文件传输
![image](https://user-images.githubusercontent.com/20842136/200115223-1f115e80-9872-4222-89ad-1db9b4d78107.png)

[Snapdrop](https://github.com/RobinLinus/snapdrop) 好用，可是经常无法访问，好消息是可以使用分支项目 [Airdope](https://airdope.io/) 代替。

# 暂时还没搞定，在 Vellum 中设置多种压力值 - Houdini
![image](https://user-images.githubusercontent.com/20842136/200117156-79180302-3b84-4a5c-bddb-f5e34c9ece0b.png)

[在 Vellum 中设置多种压力值](https://www.sidefx.com/forum/topic/87126/?page=1#post-376138)

# 如何满足小众的录屏需求？自己配置 FFmpeg 解决问题
![image](https://user-images.githubusercontent.com/20842136/200118538-926cd538-4ded-460e-ad11-61d133756ab6.png)

[如何满足小众的录屏需求？自己配置 FFmpeg 解决问题](https://sspai.com/post/76637?utm_source=weibo&utm_medium=social&utm_campaign=official)

[FFmpeg](https://ffmpeg.org/ffmpeg.html) 是处理多媒体内容（如音频、视频、字幕和相关元数据）的库和工具的集合，支持在 Linux、macOS 和 Windows 全平台运行。它提供了录制、转换以及流化音视频的完整解决方案。

# 一场很（没）有必要的春晚

![p2868013341](https://user-images.githubusercontent.com/20842136/200175506-3fdde451-9567-40e6-9942-e660820190aa.png)

[一场很（没）有必要的春晚](https://www.bilibili.com/video/BV1M34y127Xp/?spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=6c68891752436b0097051bf700e169a9)

# 小白兔白又白
![微信图片_20221105181901](https://user-images.githubusercontent.com/20842136/200115015-892af108-f308-4a12-8f66-7316cd611b5b.jpg)
![微信图片_202211051819014](https://user-images.githubusercontent.com/20842136/200115029-e8c72aed-019c-44af-b4d8-49bd61d87e38.jpg)
![微信图片_202211051819011](https://user-images.githubusercontent.com/20842136/200115018-eeeaea99-5e22-4d31-8bca-680d4bf42bea.jpg)
![微信图片_202211051819012](https://user-images.githubusercontent.com/20842136/200115023-27fe5487-f049-475c-a1e6-f7057e413a1a.jpg)
![微信图片_202211051819013](https://user-images.githubusercontent.com/20842136/200115026-e6755d04-2a29-415e-a542-ae8dad91e728.jpg)

# 后互联网时代的乱弹 第37期
<img width="957" alt="image" src="https://user-images.githubusercontent.com/20842136/200175811-c6f82b26-91eb-4cff-a6ba-dce4f1a33054.png">

**[后互联网时代的乱弹 第37期](https://www.bilibili.com/video/BV1We411F7zz/?spm_id_from=444.41.list.card_archive.click)**

# 给我一个好消息 - 李青说唱
![微信图片_20221105180742](https://user-images.githubusercontent.com/20842136/200114596-95d4f887-6487-4d42-a3de-88cd96d55c64.jpg)
