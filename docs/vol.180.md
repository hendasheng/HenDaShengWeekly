# 很大声周刊-vol.180

# text-autospace - 处理中英文混排间距问题的 CSS 属性
[text-autospace](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/text-autospace) 是一个用于处理中英文等混合排版间距的 CSS 属性。它可以自动在中文、日文、韩文字符与英文字母、数字之间添加合适的间距，同时处理部分标点附近的排版。

``` css
text-autospace: no-autospace;
text-autospace处理中英文混排间距问题的CSS属性。
```
``` css
text-autospace: normal;
text-autospace 处理中英文混排间距问题的 CSS 属性。
```

以前这类间距通常需要在内容中手动添加，或者借助脚本处理；自 2025年11月 起，此特性已在最新浏览器中得到支持。现在可以直接交给浏览器完成，而且不会修改原始文本内容，只影响最终的显示效果。

# 设计服务标准协议书
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/%E8%AE%BE%E8%AE%A1%E6%9C%8D%E5%8A%A1%E6%A0%87%E5%87%86%E5%8D%8F%E8%AE%AE%E4%B9%A6.png)

[立入禁止平面设计工作室](https://www.studionaeo.com/) 开源了一份 [设计服务标准协议书](https://github.com/studionaeo/design-services-standard-agreement) 。汇集了国内几十家独立工作室的合同样本，并参考 AIGA 的设计服务协议，再结合《民法典》《著作权法》《商标法》等中国现行法律做了本土化整理。

# Codrops｜创意网页与前端实验
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/codrops.png)
[Codrops](https://tympanus.net/codrops/) 是一个长期关注创意网页与前端实验的网站，内容主要围绕 Web 动画、交互、Three.js、WebGL / WebGPU 等方向。除了展示案例，也会拆解具体实现方式，很适合用来找网页视觉和交互参考。

# 用 Three.js 实时实现 Datamosh
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/datamoch_cover.png.webp)

Codrops 的这篇 [**教程**](https://tympanus.net/codrops/2026/09/02/breaking-the-frame-building-a-real-time-datamosh-effect-with-three-js/) 用 Three.js 和 Shader，在浏览器里实时实现了 Datamosh 效果。

传统 Datamosh 来自视频压缩出现异常时的画面错误：新画面没有被完整刷新，而是继续沿用上一帧的信息，于是旧画面的像素会被运动信息不断拖拽、撕裂，并逐渐混进新的画面里。

[作者 Niccolò Fanton](https://tympanus.net/codrops/author/niccolofanton/) 没有真的破坏视频文件，而是在 Three.js 里重新模拟了这套逻辑：保存上一帧，通过运动向量不断扭曲它，再混入少量当前画面，由此形成持续反馈的图像。后面又加入了块状压缩、错误运动向量，以及故意让部分画面无法正常更新的处理，模拟视频数据丢失时出现的块状故障。

# GPT‑6 Astra - 宣传页面的动画
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/gpt6-astra.png)
OpenAI 发布了新模型 - GPT‑6 Astra，[介绍页面](https://openai.com/zh-Hans-CN/index/gpt-6-astra/)非常值得研究，页面中的粒子图形随着滚动重组，在不同形态间过渡，还有鼠标的扰动交互，还有粒子沿着线条运动等等等，整体非常细腻。

# Oscar Dumlao 个人网站
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/oscardumlao.png)

[Oscar Dumlao](https://oscardumlao.com/) 的个人网站现在变成了一个互动水上游乐场。你可以在场景里移动、切换环境、播放音乐，而他的个人介绍和经历只是自然地藏在其中。

> 我致力于构思尚无明确形态的创意，协助团队明确开发方向，并打造能赋予新技术以具体形态的界面。
> —— Oscar Dumlao

相比传统作品集，它或许没有那么“高效”，不能一眼扫完所有项目，但结合作者对自己工作方式的介绍，这种形式反而很符合整体的气质。

# DigiShow - 开源数字表演平台
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/digishow.png)
[DigiShow](https://cdn.digishow.cn/?lang=zh) 是由[张琪 Robin Zhang](https://cdn.digishow.cn/?lang=zh) 创建的开源数字表演平台，用来连接和编排传感器、灯光、声音与空间，支持 Arduino、MIDI、DMX、OSC、ArtNet 等协议。

它更像一个面向现场表演和互动装置的“信号中枢”：不要求先写大量代码，而是通过可视化的方式把不同设备和数据连接起来，用于现场演出、交互艺术、声音与灯光控制等场景。项目目前以 Apache-2.0 协议开源，同时支持 Windows、macOS 和 Linux。

# YOLO 深度估算
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/nyu_depth_v2_web.jpg)
[Ultralytics YOLO](https://docs.ultralytics.com/zh/tasks/depth) 现在支持单目深度估计，只需要一张普通 RGB 图片，就可以预测出逐像素的深度图。

*“单目深度“指的是：只用一个普通摄像头，或者一张普通 RGB 图片，去估计画面里每个位置离相机有多远。*

*与其对应的是“双目”。双目深度会像人的两只眼睛一样，用两个不同视角之间的视差来计算距离；单目只有一个视角，没有真实的视差信息，所以它本质上是在根据物体大小、透视、遮挡、纹理等视觉线索“推测”深度。*

# 小白兔白又白
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/IMG_2911.jpeg)

# Now We Can Sing - Max Richter
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.180/Now%20We%20Can%20Sing%20-%20Max%20Richter.jpg)