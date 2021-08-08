# 很大声周刊-vol.14
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

# 种下这支花，忘了那个她
![IMG_8238](https://user-images.githubusercontent.com/20842136/128630617-f8d4255f-b498-4260-a709-4ed848b73ce1.jpeg)
<p align="center">第九周</p>

# 最近茉莉开花了
![IMG_8239](https://user-images.githubusercontent.com/20842136/128630636-267756eb-0b6c-4921-9f89-15d5c45bda39.jpeg)

这是我第一次闻到真茉莉花的味道，真香啊，倒不是特别浓烈的香，是那种走到它附近，时不时就能闻到一点香味，也不知道怎么形容了，反正真好闻。

之前闻过很多扮演茉莉香味的东西，那些都不行。

我一直喝 seesaw 家的咖啡，有一款叫小茉莉的豆子特别好，可是去年就停产了，小茉莉停产后换了另一款叫甜橙子的豆子，也挺好喝。

# 问题是这么解决的
![640](https://user-images.githubusercontent.com/20842136/128628618-71e9d484-37bc-4ade-93b9-6d45894b5bfc.png)

> 我很喜欢看李永乐老师的视频，会收获很多硬核知识。最近[《如何轻松写出加密日记？李永乐老师亲手教你制作密码盘！》](https://www.youtube.com/watch?v=32xToL3JdU0&t=194s) 这一期却让我产生了很大的困惑，倒不是内容本身，而是这张布满数字的密码盘。
> 整个密码盘分成四个矩阵，每个相邻矩阵互为镜像，我在想能不能用程序模拟这个密码盘。
> ...

![img](https://user-images.githubusercontent.com/20842136/128628762-109106f5-12c7-4418-a0c4-d129b6e3f8be.png)
我在 [问题是这么解决的](https://mp.weixin.qq.com/s?__biz=MzAxOTM5MzY1Ng==&tempkey=MTEyNV9IaVdFSXA1eXpTNmhsZ0FpT3JhS0NybHBFalJkTnpWamI1U0pGM3V6MDhmeUwxQXBpdi1sei1FMk4zVEdIN19GTDRXLWNaZWVMTWotUU54UFo5bHlSX0pmejc3bGJzandmNzZnR05qQjVSdW83NVY4eVRQZTNIeDFyMFNCa1VESWNsNzFVM0pRdU1MMzBzWVc3RG05LWhmcWhKa214NV9LbXN2T0p3fn4%3D&chksm=03ed8b3e349a02283ad0b66331239411c0e4d8745a9f2f59c1e14d773a46435a029245795f9d#rd) 文章中记录了从出现问题，到解决问题的全过程。

# Mac 升级 Git 版本
![image](https://user-images.githubusercontent.com/20842136/128628954-1096b8f8-f6ef-4d1f-a47c-f958f9023262.png)

收到 GitHub 的邮件，看的一知半解，大概应该是 git 版本问题，所以就升级一下 git 吧。

![image](https://user-images.githubusercontent.com/20842136/128629035-d8fcff41-a840-458f-82dc-f4779ec33dcc.png)
[Homebrew](https://brew.sh/) 是 macOS 端的软件包管理器，可以用它安装管理各种软件、库，只要涉及到编程，就一定离不开它。

升级 git 也需要用到 Homebrew，[《Mac 升级 Git 版本》](https://www.jianshu.com/p/6eca0eadcc22) 这篇文章解决了我所有升级过程中的疑问，尤其是 git 版本指向的问题。

# DummyImage
![image](https://user-images.githubusercontent.com/20842136/128629404-139706f6-eedb-423f-b17e-44eb0c5630cd.png)

在写 HTML 结构初期，多数情况下会用临时图片占位，提高编写速度，最后再替换正式图片。
``` html
<img src="https://dummyimage.com/600x400/b2c4ff/1928ff" alt="">
```
[DummyImage](https://dummyimage.com/) 让这件事变得更加简单、高效，它可以直接生成临时图片，并且可以在生成的链接中调整图片尺寸和颜色。

# Iconfont
![image](https://user-images.githubusercontent.com/20842136/128629481-5e2e379a-d16d-41b0-9437-63a054c7e547.png)
[Iconfont](https://www.iconfont.cn/help/detail?spm=a313x.7781069.1998910419.dfd524534&helptype=about) 是阿里巴巴出品的图标资源库，你可以在这里下载、上传图标，还支持代码应用，包含多种引用方式。

# CSS-Flex 布局
![image](https://user-images.githubusercontent.com/20842136/128629566-1139c818-69f2-4725-b491-3a538fbcce10.png)

[《Flex 布局教程：语法篇》](https://www.ruanyifeng.com/blog/2015/07/flex-grammar.html) 从 Flex 布局的由来到应用，图文并茂、深入浅出，阮一峰老师这篇文章把 Flex 布局讲的明明白白。

# 懒加载/延迟加载
![image](https://user-images.githubusercontent.com/20842136/128629694-025c2d31-69e8-43bd-a194-71a4bffc2966.png)

随着内容资源大小的增加，[懒加载](https://developer.mozilla.org/zh-CN/docs/Web/Performance/Lazy_loading)是线上应用必须要考虑的问题，懒加载的作用就是当用户需要和内容交互时，才加载内容（当滑动到某一张图片时，才加载这张图片），而不是在用户开始使用时，就加载全部内容，这样会大量浪费储存、流量资源。

[LazySizes](http://afarkas.github.io/lazysizes/#examples) 是非常好用的懒加载库，无需 JS 配置，而且文档还特别友好，在解决懒加载这件事上它可以为你节省很多时间。

# 视频懒加载
![image](https://user-images.githubusercontent.com/20842136/128629939-3468d01e-1e99-43b7-b48d-59fd1a6245e2.png)
解决图片懒加载后，紧接着就是视频的问题，我想 lazysizes 这么好用，应该也有对视频的支持吧，找了一圈没找到。后来发现 [video 标签](https://www.w3school.com.cn/tags/att_video_preload.asp)本身的属性就有相关支持（当 preload="none" 时，页面加载后不载入视频）。

# 瀑布流布局/Masonry layout
![image](https://user-images.githubusercontent.com/20842136/128630044-f9b2ef46-0b24-4413-994c-d2d018680363.png)

![image](https://user-images.githubusercontent.com/20842136/128630085-7a256b6c-21ee-4476-bf06-772a0637d57b.png)

说起瀑布流布局就不得不提到 [Pinterest](https://www.pinterest.com/) 、[Unsplash](https://unsplash.com/)，这种结构很适合展示大量卡片式内容，最近我也遇到了这样的需求。

![image](https://user-images.githubusercontent.com/20842136/128630122-754698f5-32a9-4690-be83-cc6912b9e14e.png)

[Masonry](https://masonry.desandro.com/) 是 JavaScript 瀑布流（Masonry Layouts）布局库，支持响应式布局。配置很简单，文档也足够友好，它帮我顺利地解决了瀑布流布局需求。