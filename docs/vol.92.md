# 很大声周刊-vol.92
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_92](https://user-images.githubusercontent.com/20842136/218133478-3462dc12-e450-45b1-bbe3-aa35fbfab04d.png)

# 尝试新的渲染器 - Redshift（GPU）
![image](https://user-images.githubusercontent.com/20842136/218133696-c07c099a-3c3e-420d-b591-1d6d5a957697.png)

对 [Redshift](https://www.maxon.net/zh/redshift) 早有耳闻，但一直没做尝试，因为多数输出在 Blender 中完成，内置的 Cycles 渲染器无论质量还是速度都很好， 很多在 Houdini 中完成的动态都拿到 Blender 中做材质和最终渲染，这个流程能解决多数需求，少数解决不了的就很头疼，比如属性的输出，动态 abc 文件拿到 Blender 中基本上只能识别颜色属性，其它的属性可以通过一些方法传递，但是特别复杂，还容易出错，属性和材质的关联性很强，材质没有相关属性的支持会减少很多可控项，还有粒子、曲线、体积这类文件，数据量稍大一点导入的压力就很大，后面再做材质、渲染什么的就很折磨人。

数据相互导入、导出这件事本身就很麻烦，调试成本极高，还有相关属性的兼容问题，所以后面尝试了 Houdini 自家的 [Karma](https://www.sidefx.com/products/whats-new-in-195/karma/) ，省去了导出/导入的麻烦，也不用担心相关属性没法调用，或许是还在开发中的原因吧，使用体验一般，尤其是速度，相比 Redshift / Cycles 来说慢很多。

目前的问题就是 Blender Cycles 很好，但是只能在 Blender 内部使用，Karma 能在 Houdinui 内部使用，但是不太好用，所以只能鼓足勇气，尝试新的渲染器。如果你用过任何物理渲染器，上手 Redshift 都不会太困难，只是需要熟悉一下它的工作流程和基本的运行逻辑就可以，很快就可以整活儿了。它内置在 Houdini 中，再也不用把文件倒来倒去，而且速度感人，内置的 ACES 色彩空间也很省心，基本操作都很方便，当然还有很多高阶用法，我还搞不定，回头再聊。

# Houdini 安装 Redshift
![image](https://user-images.githubusercontent.com/20842136/218136431-943c08c4-6418-4480-a53e-96b0f2193f9a.png)

[Houdini 安装 Redshift](https://www.youtube.com/watch?v=u787XP5Gbes&t=106s)

# Windows 奇妙多多 - 重启 GUP
![image](https://user-images.githubusercontent.com/20842136/218135949-26adcb19-cfbd-4de0-a0b0-712726eba92b.png)

[重启 GPU](https://twitter.com/ace5c4d/status/1437103337980235779) 的方法 **`win+ctrl+shift+b`**，和 GPU 相关的问题都可以尝试这个方法。

# Redshift - Houdini 需要注意的地方
除了上面说到的重启 GPU，在渲染的时候不要双开 Houdini，或者其它主要用 GPU 的程序，否则结果就是后台看 GPU 已经跑满，但渲染速度依然奇慢无比。

# Redshift Houdini 文档
![image](https://user-images.githubusercontent.com/20842136/218139127-2db67e98-aec6-47cd-9e84-f7892bb972be.png)

[Redshift Houdini 文档](https://help.maxon.net/r3d/houdini/en-us/Default.htm#html/Render+Settings+-+Basic.html)（不知道为什么官方文档做的这么隐蔽）

# Houdini 修复流体网格闪烁
<img width="1106" alt="2341050379207f5fafd3c1baa16a58f" src="https://user-images.githubusercontent.com/20842136/218136786-df4ca418-7586-4cf6-8415-a60c28618a12.png">

在 Houdini 中，粒子转网格后有时会出现奇怪的闪烁，很难搞，[《Houdini 修复流体网格闪烁》](https://www.youtube.com/watch?v=oSotagH9K0g) 这里的方法很管用。

# Edge Damage - Houdini 边缘磨损工具
![image](https://user-images.githubusercontent.com/20842136/218150035-b460c05a-c944-4a52-a24a-40d614ac3a23.png)

[Edge Damage - Houdini 边缘磨损工具](https://www.sidefx.com/docs/houdini/nodes/sop/labs--edge_damage-2.0.html)

# 磨损+查找边缘上色搭配用法 - Houdini
<img width="1285" alt="276_Edge_Damage" src="https://user-images.githubusercontent.com/20842136/218150741-8b168198-554f-4b0b-b0c0-60ee92c163a6.png">

[Edge Damage](https://www.sidefx.com/docs/houdini/nodes/sop/labs--edge_damage-2.0.html) + [Measure Curvature](https://www.sidefx.com/docs/houdini/nodes/sop/labs--measure_curvarture-2.0.html)

# 谷歌即将出品的人工智能 - Bard
<img width="953" alt="b6404ba5d521eeaa68c940953191a4e" src="https://user-images.githubusercontent.com/20842136/218148242-d99e55ca-38b6-4734-bbf6-1d45336b59fc.png">

[谷歌即将出品的人工智能 - Bard](https://blog.google/technology/ai/bard-google-ai-search-updates/)

# 体验一把ChatGPT：一本正经胡说八道，在中国前途难测
![image](https://user-images.githubusercontent.com/20842136/218148953-702d4217-a198-4b75-ab58-8a0f1c0c4d3c.png)

[体验一把ChatGPT：一本正经胡说八道，在中国前途难测](https://mp.weixin.qq.com/s/u_EaNic49F6WWn5-XD4HPg
)

# 小白兔白又白
![微信图片_20230211001247](https://user-images.githubusercontent.com/20842136/218140606-df67fd44-70ca-4059-852a-3f9c709907e9.jpg)
![微信图片_202302110012472](https://user-images.githubusercontent.com/20842136/218140633-9e8072b0-b498-4e2e-b67c-d2ba04885105.jpg)
![微信图片_202302110012471](https://user-images.githubusercontent.com/20842136/218140624-eb130ceb-33ae-4b44-a172-c06eda0f46e6.jpg)

# 后互联网时代的乱弹 第50期
<img width="1051" alt="image" src="https://user-images.githubusercontent.com/20842136/218311177-1e61b1c4-9fb0-4f98-8b78-ee2933bc0092.png">

**[后互联网时代的乱弹 第50期](https://www.bilibili.com/video/BV1m54y1A7Uu/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# Nous - Annael / Videoclub / Adèle Castillon
![image](https://user-images.githubusercontent.com/20842136/218149258-edc2925e-2c68-4a4f-a6da-49278c1db0df.png)
