# 很大声周刊-vol.86
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

<img width="744" alt="Snipaste_2022-12-31_22-24-25" src="https://user-images.githubusercontent.com/20842136/210139996-4c91bb8a-7710-42b1-b4d7-8038d14b012a.png">

# Houdini Remesh 节点 - UV 接缝
<img width="568" alt="302777cb564d8939b68c27b84709ee7" src="https://user-images.githubusercontent.com/20842136/210140021-3fdfbbb1-4caf-4625-9d14-27fe70df5b9a.png">

用 [Remesh](https://www.sidefx.com/docs/houdini/nodes/sop/remesh.html) 注意它对 UV 属性的影像，开启「Harden UV Seams」可以保护 UV 接缝不被细分影像。

# 获得更细腻的布料同时降低内存压力 - Houdini
![image](https://user-images.githubusercontent.com/20842136/210140457-d2bc1599-eb8d-4442-bf39-be355d7809b2.png)

[vellumpostprocess](https://www.sidefx.com/docs/houdini/nodes/sop/vellumpostprocess.html) 节点中通过 **Thickness Scale** 增加厚度获得更细腻的效果，尤其是碰撞接触面相多的时候，这个时候物体会变成两层，多数情况下内层是不需要的，所以需要删掉内层减轻内存压力。

![image](https://user-images.githubusercontent.com/20842136/210140581-951ca954-1ee0-4e67-90bf-827fb5ea865c.png)

开启 **Thickness Scale** 后，会自动增加新的分组。

![image](https://user-images.githubusercontent.com/20842136/210140614-038b098a-3e48-4efa-9ca7-93bd6bf20a48.png)

再根据需求删除多余的部分，这样可以在获得细腻效果的同时减轻一些内存压力，至少在模型上能减少 50% 的点数量。

# 复制到点后的实例抖动怎么办？ - Houdini
![210084956-d99a086c-e7da-40c5-8480-a2c664d8897b](https://user-images.githubusercontent.com/20842136/210141196-99624ce9-85c2-4a75-b45b-f2d21576a894.gif)

![image](https://user-images.githubusercontent.com/20842136/210141218-94ae1d80-85f9-4620-9b2e-9456c9202c4c.png)

[复制到点后的实例抖动怎么办？](https://www.sidefx.com/forum/topic/88004/?page=1#thumbs-up)

遇到这样一个问题，论坛中叫 tamte 的朋友给出了解决方案。

![ezgif com-gif-maker (8)](https://user-images.githubusercontent.com/20842136/210141406-f5235e85-ac01-40a1-a70f-767d1dcebb32.gif)

用到很多从来没用过的节点，暂时也没太看明白，但确实解决了问题，再继续研究一下。

# p5.play - 2D 游戏引擎 
![image](https://user-images.githubusercontent.com/20842136/210140678-541cb613-0a1a-41ae-8e49-291076be80d8.png)


[p5.play - 2D 游戏引擎](https://p5play.org/index.html)

# Device.js - 检测当前设备
<img width="1152" alt="a03aaecf2276b25090fcab9146c777c" src="https://user-images.githubusercontent.com/20842136/210140336-88d54cb9-d2df-4a79-a251-cf993c37619f.png">

[Device.js - 检测当前设备](https://github.com/matthewhudson/current-device)

检测操作系统、方向及类型，主要是操作系统的识别，可以根据对不同操作系统做相应调整。

# 几个开源音乐网站

## FMA
![image](https://user-images.githubusercontent.com/20842136/210140106-513235de-91e8-4330-8f14-9de9f1e9efd1.png)
[FMA](https://freemusicarchive.org/home)

## Jamendo
![image](https://user-images.githubusercontent.com/20842136/210140126-06ad8e7b-c920-46e4-ab93-22ec07cd4893.png)
[Jamendo](https://www.jamendo.com/start)

## LooperMan
![image](https://user-images.githubusercontent.com/20842136/210140216-10e63f7b-a749-422e-b4fc-f49d7fd43c11.png)
[LooperMan](https://www.looperman.com/free-music-software)

## FreeSound
![image](https://user-images.githubusercontent.com/20842136/210140147-d074ca3b-364e-44f9-a5f9-af13de1a13a2.png)
[FreeSound](https://freesound.org/)

# Win11 - AirPods Pro 声音变小怎么办
![image](https://user-images.githubusercontent.com/20842136/210140759-fb251d45-ef67-4df7-b1d5-5928749bde13.png)

Win11 惊喜多多，AirPods Pro 声音突然变的特别小，100% 的音量才能勉强能听清，之前还用着好好的，折腾了半天，重装驱动、删除蓝牙设备什么的都没用，[这里](https://answers.microsoft.com/en-us/insider/forum/all/low-volume-output-on-windows-11-21h2-when-compared/fa767a76-f867-470f-a213-831f58eaf64b?page=4#:~:text=%E8%BF%99%E8%A7%A3%E5%86%B3%E4%BA%86,%E7%AD%94%E5%AF%B9%E4%BA%86)是正解，还有 [《在 Windows 10 中启用或禁用蓝牙绝对音量》](https://winaero.com/enable-or-disable-bluetooth-absolute-volume-in-windows-10/?continueFlag=1bafdcd5c034def869fecb4f3bdaed70)这篇文章，说的也是这个意思。

