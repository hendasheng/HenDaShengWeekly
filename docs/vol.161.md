# 很大声周刊-vol.161
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/Title_WeChat_161.png?)

# Demucs Music Source Separation - 音源分离模型
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/9vTwM96k3mVaaWL2rgkELd9_nlNQsnK3iL3y59SKQFkb1QRnGTVy7t4gMtubTMdoxq0Sg1LPjovmewtw-N-bdfylW8Yw4KcJrlofGKKsvVbrUpWkS_vvZt3tM1W_QVKecp6T7W4kRe_WbGaI4LrbJAc3HhxQtqpp1jzUWN0za4p0stjzgX8VpKgLZ6OwE3sK.jpg)

[Demucs](https://github.com/adefossez/demucs?tab=readme-ov-file) 是开源的 AI 音频分离项目，可以将一首完整音乐拆分为 vocals、drums、bass 等独立音轨。本地运行，支持 GPU 加速。

>对于音乐家而言
>
>如果您只想使用 Demucs 来分离音轨，可以使用以下命令安装它：
>
>`python3 -m pip install -U demucs`
>

# glTF-Transform - 压缩优化 glb 模型
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/kicker.jpg)

[glTF-Transform](https://gltf-transform.dev/) 是一个专门处理 glTF / GLB 资产的命令行工具。

我在 web 3d 项目的过程中发现这个工具，web 项目对文件体积非常敏感，所以需要文件尽可能的小，它可以高效实现文件体积的优化。

# Spark 2.0 - web 端高斯泼溅渲染
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/Snipaste_2026-04-26_15-28-17.png)

[Spark](https://github.com/sparkjsdev/spark) 是一个基于 three.js 的高性能 Gaussian Splatting 渲染库，目标是在 Web 上实时渲染大规模 3DGS 场景。

# DistroAV - 在 OBS 中使用 NDI
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/DistroAV.png)

[DistroAV](https://github.com/DistroAV/DistroAV) 为 OBS Studio 提供 NDI 支持的插件，可以在局域网内低延迟传输视频与音频流。

[NDI](https://ndi.video/) 通过局域网实时传输视频与音频的协议，可以理解成“用网络代替 HDMI”。

# 高斯泼溅

## ml-sharp - 将照片转换为高斯泼溅模型
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/teaser.jpg)

[ml-sharp](https://github.com/apple/ml-sharp) 是由苹果发布的照片到高斯泼溅模型的重建工具，强调速度和质量，使用起来也方便。

## LichtFeld Studio - 面向高斯泼溅工作流的桌面工具
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/Snipaste_2026-04-26_15-43-56.png)

> [LichtFeld Studio](https://github.com/MrNeRF/LichtFeld-Studio) 专为需要比训练脚本或独立查看器更强大功能的用户而设计。它将模型训练、实时可视化、高斯编辑、导出、插件和自动化集成到一个工具链中。

## RealityScan - 现实世界数据采集
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/Snipaste_2026-04-26_15-50-38.png)

[RealityScan](https://www.realityscan.com/) 是 Epic Game 推出的采集工具，除了模型扫描外很重要的一个功能是生成包含相机位姿与图像信息的 COLMAP 数据集，上面提到的 LichtFeld Studio 需要的就是 CLOMAP 数据集。

## COLMAP 数据集
COLMAP 数据集通常指一组用于三维重建的图像与相机参数数据，包含照片、相机位置、镜头参数以及图像之间的空间关系。
简单讲它做的工作是识别并记录 “这些照片分别是从哪里拍摄的”，形成 COLMAP 数据集。
目前高斯泼溅等等相关工作流程，都建立在 COLMAP 这类数据结构之上。

## Reflct Sharp Frames - 从视频中提取适合重建高斯泼溅的画面
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/reflct.png)

[Reflct Sharp Frames](https://sharp-frames.reflct.app/) 是一个为 3DGS / Gaussian Splatting 数据准备而做的帧提取工具。

它的作用不是简单把视频切成图片，而是从视频里挑出更清晰、更适合重建的帧，尽量避开运动模糊、重复帧和质量差的画面。这样导出的图片序列可以继续交给 COLMAP、LichtFeld-Studio 等工具使用。

对于用手机或相机拍视频来做 3DGS 的流程来说，它解决的是最前面但很关键的一步：从一段连续视频里筛出真正值得拿去重建的图像。

## Sharp Frames Python
[Sharp Frames Python](https://github.com/Reflct/sharp-frames-python) 使用先进的清晰度评分算法，从视频或图像目录中提取并选择最清晰的帧。

它是 Reflct Sharp Frames 的 Python 版本。

# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/IMG_1618.jpeg)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/IMG_1581.jpeg)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/IMG_1610.jpeg)

# Drop - Cornelius
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol-161/Point-Cornelius.jpg)