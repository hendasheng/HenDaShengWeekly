# 很大声周刊-vol.17
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![125_HenDaShengWeekly-18_01](https://user-images.githubusercontent.com/20842136/131216721-eb75c3c5-bd3d-40b2-83a3-f9ea9776c169.png)

# 《标点符号用法》 GB/T 15834-2011
![image](https://user-images.githubusercontent.com/20842136/131216730-1eac2449-1005-47ee-8d46-4dbe7613cf69.png)

我们好像有点忽略标点符号这事儿了，[《标点符号用法》 GB/T 15834-2011](http://www.moe.gov.cn/ewebeditor/uploadfile/2015/01/13/20150113091548267.pdf) 是最新的标点符号用法（国家标准），没事看看，挺好。

![ezgif com-gif-maker (4)](https://user-images.githubusercontent.com/20842136/131217065-d178e031-82b7-4e33-aaf0-fd316d2f8a65.gif)

这是我为《标点符号用法》制作的动态封面。

# Processing 引入 Json
![image](https://user-images.githubusercontent.com/20842136/131217051-9c5a0a33-61c5-403b-8a9a-e5e929c4df97.png)

制作《标点符号用法》动态封面时，把所有标点符号文本保存到一份 Json 文件中，后期方便引用，可是有点记不清 Processing 引入 Json 的具体方法了，好在之前写过一篇文章 [《向数据可视化迈出一小步》](https://mp.weixin.qq.com/s?__biz=MzAxOTM5MzY1Ng==&mid=2648609958&idx=1&sn=e7de17cea10551622eedbca6c6727dd1&chksm=83ed89b1b49a00a7251192b2551896cef76f074391aa85631074c1a793d3043f5e62a17540e6&token=926645855&lang=zh_CN#rd)，再加上脑海中的印象，很快就能熟悉起来。

这种类似笔记的文章写的时候很头疼，感觉就是把已经掌握的东西记录一下，没什么意思，谁知道这东西后劲大，一段时间之后再看会很有帮助，能节省不少时间。

好在以文章的形式记录了一下，好在没高估自己的记忆力。

# typo.css - 中文排版
![image](https://user-images.githubusercontent.com/20842136/131322781-86be6bd7-2d03-4ff6-a52a-586a6ec41fc5.png)

最近在研究中文标点符号，在使用标点符号时只考虑用法是否规范就好，可是在排版上还有很多问题。

![download-2](https://user-images.githubusercontent.com/20842136/131325481-19016541-d634-4dc6-bee4-e304c5c0672c.jpg)

比如着重号，Unicode 中就没有收录，所以我们根本没办法输入这个符号。

![download](https://user-images.githubusercontent.com/20842136/131325494-33b7ac30-fe32-46ea-9787-e0cdace1d821.jpg)

偶然发现 [typo.css](https://typo.sofi.sh/?continueFlag=a1a6353bf5ecaab87f6453281fff0fb2) 居然通过 css 的方式实现了着重号，太厉害了。

# WebP - 一种用于 Web 的图像格式
![image](https://user-images.githubusercontent.com/20842136/131217107-65f38fac-088c-4ab8-ae89-00e1050f859a.png)
> WebP 是一种现代图像格式，可为网络上的图像提供卓越的无损和有损压缩。使用 WebP，网站管理员和 Web 开发人员可以创建更小、更丰富的图像，从而提高 Web 速度。

![download-2](https://user-images.githubusercontent.com/20842136/131217309-1992bbdd-8fae-47d5-b92e-117f7fd92c7c.jpg)

最近做[个人网站](https://hendasheng.com/)才了解到 [WebP](https://developers.google.com/speed/webp) 格式。测试网站性能时（[PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)），发现原来的图片格式（png）会拖慢速度，提示中建议用 WebP 格式，试了一下果然有很大的差异，以下是同一张图片，两种不同格式的对比。

![img](https://personal-website-resources.oss-cn-hongkong.aliyuncs.com/web/ProjectImage/HenDaShengWeekly/HenDaShengWeekly_WebCover_01.png?x-oss-process=image/format,webp)

![image](https://user-images.githubusercontent.com/20842136/131217266-60b45b13-ad2b-46f8-b840-7105ad235d3b.png)

![download-1](https://user-images.githubusercontent.com/20842136/131217453-e6f1fc90-a8b7-4837-b343-0e32a5719b93.jpg)

调整图片格式后，网站加载速度有了明显提升。

# 转换图片格式
[个人网站](https://hendasheng.com/) 用的图片储存服务是阿里云的 [对象储存 OSS](https://www.aliyun.com/product/oss?spm=5176.19720258.J_8058803260.33.7bd22c4afBTrph)，除了储存服务外，它还提供很多功能，包括图片处理。

![image](https://user-images.githubusercontent.com/20842136/131217577-1d0645ea-09a2-4c3c-98d6-74d4a33e230a.png)

在原链接的基础上增加相应的参数就可以进行图片处理，非常方便。

最开始意识到需要调整图片格式时很头疼，因为图片量很大，我能想到的只有手动调整，最多想到批量调整格式，直到发现 OSS 这个功能，，写一个 js 脚本，遇到 `.png || .jpg` 这样的链接，就自动在后面添加转换格式参数。这个功能让修改格式这件事瞬间轻松了很多。不过过程中还有点小发现，gif 格式不能转换成 webp。

# Processing 引入 svg
![sketch_133_HandmadeLeatherTools_01](https://user-images.githubusercontent.com/20842136/131217845-daf4979b-2e55-4a64-82bc-d0bc65545b99.gif)

我用 Processing + svg 的方式完成了这个动画，过程中遇到 Processing 引入 svg 的问题。

当 Processing 引入相对复杂的 svg 图形时，很容易显示错误。

![image](https://user-images.githubusercontent.com/20842136/131218111-f59da321-edc3-4d37-9e44-e8ca24e354fc.png)

这个时候要在画 svg 图形的工具（Figma 为例）上检查一下，这个图形是否有过多的布尔操作。

![image](https://user-images.githubusercontent.com/20842136/131218159-08ffed68-96f2-4552-af34-8de085ff8e0e.png)

![image](https://user-images.githubusercontent.com/20842136/131218375-d49c1196-0fcf-42f8-b0f0-6d2fea96cca4.png)

如果有很多布尔操作，把复合图形变成单一图形（Figma 上这个功能叫 `Flatten`，其他软件中一定有类似功能），在 Processing 上就能正常显示。

这只是我在遇到 Processing 引入 svg 显示错误时的应方法，还搞不清什么原理，但总是管用。

还有，如果你要设置 svg 填充色，记得开启 `P2D` 模式。

# Year #20 - Processin 20 周年活动
![img](https://user-images.githubusercontent.com/20842136/131323121-1ed80607-e99d-4214-b70b-9703e0b81c5f.png)
[Year #20](https://openprocessing.org/curation/70077) 是 [OpenPorcessing](https://openprocessing.org/) 为庆祝 Processing 20 周年举办的活动，有一定的创作规则，每个人都可以发布，[我的](https://openprocessing.org/sketch/1250839)好像有点跑题。

![image](https://user-images.githubusercontent.com/20842136/131324367-3576fec0-ccd9-4a49-a74c-211eccd43b60.png)

最喜欢的是 [Senbaku 的作品](https://openprocessing.org/sketch/1247092)，颜色和纹理处理的非常精彩。