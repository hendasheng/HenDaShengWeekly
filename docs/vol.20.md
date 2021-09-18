# 很大声周刊-vol.20
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![sketch_140_HenDaShengWeekly_vol-20_01](https://user-images.githubusercontent.com/20842136/133735323-806543e1-0c24-434d-83a1-d8a92ba632e3.png)

# Unsplash API
![image](https://user-images.githubusercontent.com/20842136/133735437-1ef6f52d-1f36-4168-9076-9fbbab0a6b69.png)

 [Unsplash](https://unsplash.com/) 开放的功能接口，包含很多功能，在 [Unsplash API](https://source.unsplash.com/) 中详细介绍了功能及用法。

 # Web 线上调试环境
 ## JSFiddle
 ![img](https://user-images.githubusercontent.com/20842136/133735994-d5d1741c-488c-4191-8c43-e78447f91e0b.png)

## CodePen
![img](https://user-images.githubusercontent.com/20842136/133736209-40371c76-39b2-4a66-bb6a-24234349bd8a.png)


[JSFiddle](https://jsfiddle.net/) 和 [CodePen](https://codepen.io/your-work) 是两款线上 Web 调试应用，环境和基础代码都已经准备好了，直接在上面写自己的核心代码可以，做测试的时候可以节省一点时间，在提问的时候也非常方便，直接分享代码链接，对方可以很直观地看到代码。

相比之下我更喜欢 [JSFiddle](https://jsfiddle.net/)，它支持代码自动填充。

# 为什么苹果会制霸下一个十年？【AR增强现实】写在 iPhone 13 发布之前
![image](https://user-images.githubusercontent.com/20842136/133736952-9410a445-3d65-4ae7-b921-1e86aee08619.png)
> 早在手机市场杀成一片红海之前，苹果就已超前布局，将航向对准了下一代人机交互平台——AR增强现实
> 这个视频可能是你能找到的最全面的苹果AR战略分析。
> —— [暗流啊暗流](https://space.bilibili.com/4059187?spm_id_from=333.788.b_765f7570696e666f.2)

介绍中主要针对 AR，看完视频后不仅对 AR 有了更深入的认识，

作者在介绍 AR 的同时，顺便也聊了聊 VR，看完视频后不仅对 AR 有了更深入的了解，对 VR 也有一些的认知。

# Processing / P5js 矩阵排列计算差异
![cbb9ab69cdf2a77f2eb01100f959553e92d67f7b](https://user-images.githubusercontent.com/20842136/133737843-5db33059-bf8d-4287-b0ba-0d3782a0596a.png)

![413cc38a958e5d407a66119d8f3ac4587c075248](https://user-images.githubusercontent.com/20842136/133737848-4778f88a-ef1a-484a-9224-5a293b811640.jpg)

同样一套计算方式，在 Processing（图1）和 P5js（图2）上出现了不同的结果，折腾半天发现问题出在数据类型上。

![001PXgh3ly1guijbzjejoj619c0fqzn002](https://user-images.githubusercontent.com/20842136/133738313-4f103822-c1eb-4ef2-ab83-b2dc1f3bf059.jpg)

[Processing / P5js 矩阵排列计算差异](https://discourse.processing.org/t/processing-p5-js-matrix-arrangement-calculation-difference/32265)

Processing（Java）声明变量时需要明确数据类型，而 js 不需要这样，如果代码中涉及到计算，Processing / P5js 转换时就有可能出现类似问题，要留意数据类型。

# 设计师如何拥有自己的个人网站（二）
![ff0cde4830ac5e011c10422693ffee88](https://user-images.githubusercontent.com/20842136/133738884-c8bee658-1fe7-4e01-9103-51665528790e.png)

[《设计师如何拥有自己的个人网站（二）》](https://sspai.com/post/68759) 接着 [上一篇](https://sspai.com/post/68670) 聊了聊服务器、域名等等关于网站上线的相关问题。

# P5js 插入到 html 中（支持 CSS 和响应式）
![img](https://user-images.githubusercontent.com/20842136/133890585-81d90438-481e-40cb-98e5-c89cee303124.png)

[P5js 插入到 html 中](https://mp.weixin.qq.com/s?__biz=MzAxOTM5MzY1Ng==&mid=2648610553&idx=1&sn=a6928da6ca2abcca2402d0dbb1bb0593&chksm=83ed8beeb49a02f8e99728a02a9afc39672843f488ca54384e2c8c853c1cb302483394967c66&token=1025703500&lang=zh_CN#rd)

# NormalMap Online 在线转换法线贴图
![image](https://user-images.githubusercontent.com/20842136/133890849-47208b42-be60-464b-b91c-49323d5b9121.png)

上传黑白贴图后 [NormalMap Online](https://cpetry.github.io/NormalMap-Online/) 会帮你自动生成法线贴图，并且提供了一些可调整参数。

# HTML video 标签微信端 bug
发现新的 bug，在微信上打开 [很大声 Web](https://hendasheng.com/)，页面中的视频不能正常播放，当点击「播放」按钮后，视频不加载，而是一直显示封面图片。

我想问题出在 `<video>` 标签的 `preload` 属性上，目前设置 `preload="none"`，也就是页面打开后不加载视频，当用户点击「播放」按钮时才加载，这样可以减轻浏览器负担，也能帮用户节省流量，可能是微信对这个属性的支持不好，所以出现点击「播放」按钮，视频不能按预期加载的 bug，所以需要在点击「播放」时，强制加载，把 video 标签的 preload 属性设置为 “auto”，果不其然，通过这样的设置顺利解决了问题。

现在在微信上打开 [很大声 Web](https://hendasheng.com/)，页面中的视频也可以正常播放了。

# 中秋节
明天就是中秋节啦，各位节日快乐。

![153774623711677e8326bea](https://user-images.githubusercontent.com/20842136/133890648-f36d6743-2778-438c-a0d5-0ae57fe22d12.jpg)
*图片引用自网络*