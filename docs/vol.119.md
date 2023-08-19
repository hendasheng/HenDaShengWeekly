# 很大声周刊-vol.119
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_119](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3f2e8367-3ff9-4763-ab84-6f9938571fcb)

# Houdini 通过 FFmpeg 输出预览视频 .mp4
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/796d956e-b7a7-47c5-a7be-ff3c004c14a2)

一直以为 Houdini 中内置了 FFmpeg 方便输出，最近发现并不是这样，如果你的电脑中没有安装过 FFmpeg，它不会出现在输出选项中的。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b9875155-3317-4764-82d0-b0f873e1ee9c)

[安装 FFmpeg 并设置环境变量](https://www.youtube.com/watch?v=PLbijyGIAEo&t=23s)，Houdini 会自动在系统中识别，这样可以更方便地输出预览视频。

# Houdini Flipbook 可能报错的原因
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/616146ae-5a24-41e0-b5a0-53c1043508e5)

在非 100% 的情况下，输出视频时有一定概率报错，说编码错误啥的，100 % 就不会出现这个问题。

核心在于分辨率，当出现奇数时就会报错，比如 1500 * 2000 的 75%，也就是 1125 * 1500，这样就会报错，当恢复到 100% 时则正常输出。

反正分辨率别是奇数就对了。

# Omniverse - NVIDIA 推出的 3D 协作平台
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/6b8d453d-31c1-4e4f-a2b5-9ec790329f24)

NVIDIA Omniverse™ 是一个计算平台，使个人和团队能够开发通用[场景描述（USD）](https://www.nvidia.cn/omniverse/usd/) - 基于三维工作流和应用程序。

## Omniverse Nucleus 本地服务器
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/32e83df4-6d1f-4a37-93ce-0fbdd7b64d7f)

[Omniverse Nucleus](https://docs.omniverse.nvidia.com/nucleus/latest/index.html) 是 Omniverse 的核心功能，通过它创建本地服务器才能完成协作。

过程中我遇到这样的问题，创建服务器时在确定用户名/密码没问题的情况下，提示“用户名或密码错误”。找了一圈有类似问题，可以并没找到有效的解决方案。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/583a0112-fdd3-457d-9be5-aa8d2946f0b0)

直到遇到这个[答案](https://forums.developer.nvidia.com/t/cant-login-in-localhost-3009/165766/2#:~:text=%E6%AD%A4%E5%A4%96%EF%BC%8C%E4%BD%9C%E4%B8%BA%E9%AA%8C%E8%AF%81%E7%99%BB%E5%BD%95%E5%8A%9F%E8%83%BD%E6%98%AF%E5%90%A6%E6%AD%A3%E5%B8%B8%E5%B7%A5%E4%BD%9C%E7%9A%84%E6%95%85%E9%9A%9C%E6%8E%92%E9%99%A4%E6%AD%A5%E9%AA%A4%EF%BC%8C%E6%82%A8%E5%8F%AF%E4%BB%A5%E5%B0%9D%E8%AF%95%E4%BD%BF%E7%94%A8%20admin/admin%20%E4%BD%9C%E4%B8%BA%E7%94%A8%E6%88%B7/%E5%AF%86%E7%A0%81%E3%80%82)，抱着试一试的心态，果然可以，用最质朴的方式解决了这个问题。

# FFmpeg 还能压缩图片
`ffmpeg -i input.png -vf "scale=1920:-1" output.png`

[ffmpeg 压缩图片](https://juejin.cn/s/ffmpeg%20%E5%8E%8B%E7%BC%A9%E5%9B%BE%E7%89%87%E5%A4%A7%E5%B0%8F)

# Houdini 展 UV
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1c3a6900-d2d2-4b8e-b80e-361d21980bc3)

[Houdini 展 UV](https://www.youtube.com/watch?v=VNX9Qf6a5hs&t=14s)
这个视频将是关于展 UV 的！创建 UV 的方法有很多种，并且更加程序化。在这里您将看到 Houdini 提供的大部分展开节点。

# Open Stage Control - OSC / MIDI
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3d4a4570-7f94-4416-aefd-2f6ac41ef47a)

[Open Stage Control](http://openstagecontrol.ammd.net/docs/getting-started/introduction/#overview)，自由和模块化 OSC / MIDI 控制器（PC / 移动端）。

# Blender + OSC 控制
![ezgif com-optimize (5)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b5e6c431-ae08-483c-a182-aa453864c810)
需要用到 [NodeOSC - Blender](https://github.com/maybites/blender.NodeOSC)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/6ba0d8c2-2818-43ea-a099-4070c24ee369)

安装好 NodeOSC 后，在可控项右键菜单中会出现 “Create a node osc handler” 的新选项，它会帮你自动把路径加载到插件中。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/84e41dcc-faba-4e3f-af23-1363c27b0bb6)

有一个问题需要注意，在控制矢量（位置、旋转 ...）时，需要手动调整路径。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ee140b0a-fa7d-46ac-80fc-a4c67887c013)

比如把 x 轴位移作为控制项，路径显示为 `bpy.data.objects['Cube.001'].location`，这种情况下是无效的，因为 x/y/z 轴都可以写成这样，当你需要明确具体轴向时，需要在后面加索引值，如： `location[0]` 代表 x 轴，`location[1]`、`location[2]` 则是 x / y 轴。

# 小白兔白又白
![微信图片_20230819193536](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2ad4abeb-9979-493b-9d30-95a720f03b25)
![微信图片_202308140014141](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/9c17fe5f-a024-4dbc-9aae-f7b86734b3a6)
![微信图片_202308140014172](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/933dd5b6-e0f7-4fe9-96b3-bb4548a4fa44)
![微信图片_202308140014173](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/39878f32-c1ca-4d6e-8a0c-c6e7d89141df)

# 持续三年的晕眩 - 伤心欲绝
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/313c570b-8658-4e54-b708-5e75b86b97ce)
