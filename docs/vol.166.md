# 很大声周刊-vol.166

# RF-DETR Real-Time - 实时检测
上周尝试了 [YOLO](https://docs.ultralytics.com/zh) ，对于离线视频检测来说，YOLO 已经完全能满足我的需求，可以识别画面中的目标，输出检测框和追踪数据。

我可以把检测结果拿到前端使用，但尝试把它用于摄像头实时检测时，效果并不理想，主要问题不是“能不能检测”，而是实时性、延迟和整体流畅度还没有达到我想要的状态。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/ef-detr-huggingface.png
)
之后看到了 Hugging Face 上的 [RF-DETR Realtime Webcam demo](https://huggingface.co/spaces/huggingface-projects/rf-detr-realtime-webcam)，实时运行完全没问题，所以尝试用 [RF-Detr](https://github.com/roboflow/rf-detr) 完成实时检测，目前还在进行中，但是作为实时应用是完全可行的，接下来我会尝试把实时数据作为视听觉的控制系统的一部分。

# RedShift Houdini 安装位置变更
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/rs-houdini.png)

RedShift 26.4.0+ 版本，安装位置变更。
```
C:\ProgramData
变更为 👇
C:\Program Files\Maxon Redshift
```

如果你是通过 Houdini Package JSON 方式加载 Redshift，需要同步修改 packages/redshift.json 里的路径。

# The VFX Mentor - COPs
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/thevfxmentor-cops.png)

[The VFX Mentor 整理了一个 Houdini COPs](https://thevfxmentor.com/quicktips/COP/) 的基本入门页面，
内容覆盖 COPs、Feedback Loop、COPs 与 SOP / Karma 的互通，以及 OpenCL 生成图像的基础写法。对于想把图像数据直接参与几何生成、材质控制或程序化纹理制作的 Houdini 用户来说，这是一个很实用的速查页面。

[新版 COPs](https://www.sidefx.com/docs/houdini/nodes/cop/index.html) 不再只是“合成”，而更像是可以接入 Houdini 各个网络的数据处理层。


# Houdini Vex 色相/饱和度/明度控制
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/houdini-set_HSV.png)

``` C
float hue_shift = chf("hue_shift");          // 色相偏移 (0~1)
float sat_mult  = chf("saturation_mult");    // 饱和度倍数
float val_mult  = chf("value_mult");         // 明度倍数

vector hsv = rgbtohsv(@Cd);

// 色相调整并循环 0~1
hsv.x += hue_shift;
if (hsv.x > 1.0) {
    hsv.x -= 1.0;
}
else if (hsv.x < 0.0) {
    hsv.x += 1.0;
}

// 饱和度调整
hsv.y *= sat_mult;
if (hsv.y > 1.0) hsv.y = 1.0;
else if (hsv.y < 0.0) hsv.y = 0.0;

// 明度调整
hsv.z *= val_mult;
if (hsv.z > 1.0) hsv.z = 1.0;
else if (hsv.z < 0.0) hsv.z = 0.0;

// 转回 RGB
@Cd = hsvtorgb(hsv);

// @Alpha = chf("Alpha");


```

# OpenMAIC -开放式多智能体,互动课堂平台
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/openmaic-home.png)

>[ OpenMAIC](https://openmaic.io/zh/#getting-started)（Open Multi-Agent Interactive Classroom，开放式多智能体互动课堂）是由清华大学开发的开源 AI 平台，能够将任何主题或文档转化为沉浸式的互动课堂体验。它通过 LLM 驱动的 AI 教师和同学进行多智能体编排，提供个性化、引人入胜的课程。

---

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/openmaic-guitar-lessons-01.png)

我尝试生成吉他音程/音阶的课程，还没深度体验，但初期体验已经很好了。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/openmaic-guitar-lessons-02.png)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/openmaic-guitar-lessons-03.png)

不只给出文本讲解，还有阶段性的测试和交互页面，尤其是交互页面，这个体验很重要，把知识点拆分成适合的感知方式，比如音阶相关，只有真正听到大三度、小三度这些声音关系，概念才会变得清晰。

# 随时随地使用 Codex
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/16_9.webp)

[Codex 现已登录 ChatGPT 移动应用](https://openai.com/zh-Hans-CN/index/work-with-codex-from-anywhere/)，因此无论你身在何处，都能随时掌握进展；同时，Codex 还能在你的笔记本电脑、开发机或远程环境中持续完成工作。

随着智能体开始承担运行时间更长的工作，一种新的协作节奏正在形成。为了让工作持续推进，你需要能够轻松回答问题、查看 Codex 的发现、调整方向、批准下一步操作，或加入新的想法。

# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/IMG_1988.jpeg)


# Give Me an Answer - Low Roar
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.166/Give%20Me%20an%20Answer-Low%20Roar.jpg)