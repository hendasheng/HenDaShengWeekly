
# 很大声周刊-vol.01

## 月球贴图
适合在 CG 中使用的月球贴图（NASA Scientific Visualization Studio），分辨率让人感动。

![image](https://user-images.githubusercontent.com/20842136/117564348-2d0d3280-b0de-11eb-8c30-2870d03c8707.png)
https://svs.gsfc.nasa.gov/4720

**教程**
![image](https://user-images.githubusercontent.com/20842136/117564393-680f6600-b0de-11eb-904b-fc3a87ca469e.png)
https://www.youtube.com/watch?v=3dlSLviiX70&list=LL&index=3
我也跟着尝试了一番。
![image](https://user-images.githubusercontent.com/20842136/117564426-8d03d900-b0de-11eb-93f8-8032543f9d01.png)
***

## Blender Eevee 玻璃材质 - CGVertex
Blender 有两款渲染器（Eevee / Cycles），Eevee 是实时渲染引擎，基于 OpenGL 构建，采用一种叫光栅化的算法渲染画面，可以极大地加快渲染速度，但同时也存在很多限制。即便是这样，第一次使用时仍然被实时渲染震撼到，我的很大一部分作品都是使用 Eevee 渲染。Cycles 基于物理路径追踪，能够提供更为细腻、真实的渲染效果，可是渲染时间要比 Eevee 更久一些。
![image](https://user-images.githubusercontent.com/20842136/117564444-ae64c500-b0de-11eb-886c-ffc7b6eb8d9e.png)
最近的练习中用到玻璃材质，玻璃材质在 Eevee 上表现不是很好，以前遇到这种需求就立刻转移到 Cycles 上，最近正好看到一个教学视频，关于在 Eevee 中的玻璃材质教学，看完视频后发现，我以为的玻璃材质在 Eevee 上表现不好，更多是因为我不会用。
![image](https://user-images.githubusercontent.com/20842136/117564462-bcb2e100-b0de-11eb-854e-09d7bdb36b77.png)
https://www.youtube.com/watch?v=rBOHa_jVVRU&list=LL&index=1
更准确的而说法应该是，玻璃材质在 Eevee 上需要更复杂的设置才能达到理想效果，Eevee 并不是基于真实物理计算，所以“更复杂的设置”就像是帮 Eevee 更好地理解玻璃应该是什么样子，虽然做了复杂的设置，但渲染速度依然香甜。
***

## 3D材质-Julio Sillet 3D Art
![image](https://user-images.githubusercontent.com/20842136/117564493-dd7b3680-b0de-11eb-8fa6-eaed16bc7bcf.png)
https://gumroad.com/juliosillet?sort=page_layout
作者主页介绍写到：“为所有人制作免费的 3d 和 Blender 内容”，分享了大量高质量的材质。
***

## p5.js 演示
![image](https://user-images.githubusercontent.com/20842136/117564513-f7b51480-b0de-11eb-8d84-63ad8ff65988.png)
https://p5-demos.glitch.me/
使用 p5.js 进行生成艺术，动态图形和交互式设计的一些示例（开放源码）。
受作者启发，我也很想做一个这样的合集，把日常练习放在里面。
***

## 色差 + 运动模糊
#### Dave
![image](https://user-images.githubusercontent.com/20842136/117564537-14514c80-b0df-11eb-8b9c-4ab8dc0b6fc3.png)
[dave @beesandbombs](https://twitter.com/beesandbombs/media) 在作品中经常用到色差+运动模糊，非常漂亮，还分享了[效果模版](https://gist.github.com/anonymous/10675250)，这套模板是在 7 年前上传的，我在测试的时候是没办法运行的，里面用到很奇怪的语法，很可惜，我还没有修复它的能力，如果你也感兴趣就动手尝试一下吧。
#### Jeff
![image](https://user-images.githubusercontent.com/20842136/117564575-4d89bc80-b0df-11eb-82af-a7b6c920a4f4.png)
https://ippsketch.com/posts/chromatic-motion-blur/
[Jeff @ippsketch](https://twitter.com/ippsketch) 在 Dave 的基础上，用 p5.js 实现了同样的效果，并且很详细的介绍了过程（并不是简单的移植，Processing 和 p5.js 对于像素的处理机制不同），最终用两种方法实现了效果。
***

## 如何在 GitHub 自述文件中添加图片
尝试建立仓库的时候遇到了这个问题，常规做法是把图片也存到仓库内，需要用到的时候引用相对路径，但是文章中会出现大量图片，先保存到文件中再引用，这种做法很麻烦。

![image](https://user-images.githubusercontent.com/20842136/117564841-a574f300-b0e0-11eb-89cf-0585fc8a30f8.png)
[README images in Github](https://www.youtube.com/watch?v=nvPOUdz5PL4)，视频作者给出了相对快捷的方法，在 github 中随便打开一个有输入框的页面，把图片拖到输入框内，github 会把图片上传到服务器，并生成链接，在自述文件中粘贴这个链接就完成了图片的置入。
