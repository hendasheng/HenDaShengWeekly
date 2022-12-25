# 很大声周刊-vol.85
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_85](https://user-images.githubusercontent.com/20842136/209430743-80cf3eda-47f7-40ce-b692-5970501b5083.png)

# 关于 WebAR 的尝试
最近在尝试 WebAR 应用，主要用到  [AR.js](https://ar-js-org.github.io/AR.js-Docs/)（图像、位置跟踪）、[MindAR.js](https://hiukim.github.io/mind-ar-js-doc/)（多图像、面部跟踪）、[ARKit](https://developer.apple.com/cn/documentation/arkit/)（3D 投射）。前两者理论上是全平台支持，后者基于 iOS 设备，只是在浏览器端留出调用 iOS 摄像头和运动功能的接口，只支持 iOS 11.0+ 设备。

AR.js 和 MindAR.js 都基于图像跟踪，但后者体验更好，文档也相对友好。

3D 部分 ARKit 体验超棒，搭建起来也简单，可是只支持 iOS 设备，这就有点尴尬，本来做 WebAR 就是希望浏览器打开就能用，摆脱设备、应用的限制，但是 ARKit 真的很好啊，前面忘了说 MindAR 也有 3D 功能，只是没办法像 ARKit 那样做空间运算，它必须有目标图像才能正常运行。

# Three.js + AR.js 测试 - stemkoski
![image](https://user-images.githubusercontent.com/20842136/209432319-49107adf-2aa0-4649-a72a-00074d32aab5.png)

前面提到的 AR.js、MindAR.js 都是基于 Three.js 实现的，通过 [Three.js](https://threejs.org/) 可以实现更高阶的功能， [stemkoski](https://github.com/stemkoski/AR-Examples) 的 [Three.js + AR.js 测试](https://stemkoski.github.io/AR-Examples/) 是一套有指导意义的示例集合。

# 使用 Three.js + AR.js 实现 WebAR - 君冢
![20210303170458](https://user-images.githubusercontent.com/20842136/209432508-9eca807f-0a82-4cff-8dc6-9fbc9223d299.gif)

[使用 Three.js + AR.js 实现 WebAR - 君冢](https://blog.kimizuka.org/entry/2021/03/03/175450)

# 什么是速度？- Houdini
![image](https://user-images.githubusercontent.com/20842136/209433067-bf866a6b-734d-4138-8580-781e9303b849.png)

[什么是速度？](https://www.youtube.com/watch?v=wNLxXMWwkxk&t=8s) 介绍了 Houdini 中关于速度的

Houdini 在动力模拟方面的能力众所周知，而速度是动力模拟中最重要的变量，视频中介绍了关于速度值的相关信息。

# Houdini VEX - Chramp 用法
![image](https://user-images.githubusercontent.com/20842136/209432587-40df53be-918e-4739-a249-4b9c537bd99a.png)

![Chramp_waves_demo](https://user-images.githubusercontent.com/20842136/209432614-6d86d115-b75b-4535-a08d-a6c209738d72.gif)

[Houdini VEX - Chramp 用法](https://www.tokeru.com/cgwiki/index.php?title=JoyOfVex4)

# 金丝雀 - Rodeo FX
![image](https://user-images.githubusercontent.com/20842136/209432704-79b486c7-a621-49b1-99e6-29719143b001.png)

[金丝雀 - Rodeo FX](https://www.sidefx.com/community/canary/) 介绍了短片中金丝雀的制作过程，也没太看明白，反正挺难的。

![image](https://user-images.githubusercontent.com/20842136/209432892-b956b852-7121-4040-9154-17ed24ab7e32.png)

特效团队 - [RodeoFX](https://www.rodeofx.com/)

# 中南海新包装
![e39df1d2cfbc222ca2fccc147499d7d](https://user-images.githubusercontent.com/20842136/209463075-f9612d27-8275-4693-a99c-754ac6c01c53.jpg)

# Dynamic Wallpaper Club - MacOS 动态壁纸
![image](https://user-images.githubusercontent.com/20842136/209463256-8fafc9a7-e4c3-4935-9afc-bf1177d4800e.png)
[Dynamic Wallpaper Club](https://dynamicwallpaper.club/)

# 后互联网时代的乱弹 第44期
![image](https://user-images.githubusercontent.com/20842136/209463961-a5022a8e-6617-424a-a4c0-2b0b29ecb9df.png)

**[后互联网时代的乱弹 第44期](https://www.bilibili.com/video/BV1He4y1j7oY/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# 肥蝶他久久不能离去 - 超级市场
![image](https://user-images.githubusercontent.com/20842136/209463218-b979dff8-98bc-42f9-bc37-2356691766c5.png)
