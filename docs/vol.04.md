# 很大声周刊-vol.04
很大声周刊，在这里记录日常工作、生活所见，每周一发布。
***
![74_HenDaShengWeekly-04_01](https://user-images.githubusercontent.com/20842136/119775215-e6993f80-bef5-11eb-8416-8f0e6ee5622a.png)

# Duck 3D - Blender
![image](https://user-images.githubusercontent.com/20842136/119775453-324be900-bef6-11eb-9b9d-8c313708bea8.png)

[Duck 3D](https://www.youtube.com/channel/UCuNhGhbemBkdflZ1FGJ0lUQ/featured) 是一位 Blender 教学博主，他并没有按照线性的知识点逐个讲解，而是通过实际案例，引申出相关知识点。这种方式对观看者来说印象更为深刻，对于工具实际应用效果也有更直观的了解，很容易举一反三。

本期周刊封面就是看到 [刚体力学制作抽象文本动画](https://www.youtube.com/watch?v=n-jIIvhpwms&t=892s) 之后，加上自己的想法完成的。

使用 Blender 以来，Duck 3D 的课程给我很大的帮助。
***
# 将图形转换为贝塞尔曲线
最近在项目中遇到关于 svg 图形的问题，Processing 本身支持导入 svg，可是有很多限制，相对复杂的 svg 图形（有镂空或者经过布尔运算的）还容易出错，所以在想有没有可能把 svg 转换成贝塞尔曲线，这样用起来会方便很多。

想了很久都不知道该怎么办，我掌握的东西解决不了这事儿。

## Processing Foundation
![image](https://user-images.githubusercontent.com/20842136/119779117-e3ed1900-befa-11eb-9c59-bdeba3a8e1a2.png)

[Processing Foundation](https://discourse.processing.org/) 是 Processing/p5js 的官方论坛，里面包含了大量的问题和答案。在我遇到问题的时候都会来这里看看，很多时候都能找到解决方案。

你遇到的问题，通常不是你第一个遇到的，论坛这种形式在这里发挥了最大价值。你遇到的问题，很可能已经有解决方案在论坛中等着你了，甚至还引申出更多内容。

我的问题是怎样把 svg 图形转换成贝塞尔曲线，[noel](https://discourse.processing.org/t/imported-svg-is-pshape-group-cannot-convert-to-arraylist-of-pvector/22642/3?u=niuuin) 在一个帖子中的回答就完美地解决我遇到的问题。

![image](https://user-images.githubusercontent.com/20842136/119790602-a68e8880-bf06-11eb-8847-e1272f32bc9b.png)

![image](https://user-images.githubusercontent.com/20842136/119790716-bb6b1c00-bf06-11eb-906a-5ac6bd40fdd5.png)

把图形保存成（白色底、黑色图形）图片，经过处理，就能得到这个图形的贝塞尔曲线数据，直接就可以拿到你的项目中使用。

# The Coding Train
![image](https://user-images.githubusercontent.com/20842136/119786483-d0de4700-bf02-11eb-921d-ccc53dee852d.png)

即便大家可能都知道，但还是要介绍一下 [The Coding Train](https://www.youtube.com/channel/UCvjgXvBlbQiydffZU7m1_aw)，是 [Daniel Shiffman](https://shiffman.net/) 的 YouTube 频道，[Daniel Shiffman](https://shiffman.net/) 是纽约大学 ITP（Interactive Telecommunications Program）副教授，长期在网络上分享他的课程，几乎每个学 Processing / p5js 的同学都看过他的课程吧，从入门到后期的深入，面面俱到，不看不行。

还有两本书， [《Processing 编程指南》](https://book.douban.com/subject/26992338/)[《代码本色》](https://book.douban.com/subject/26264736/)，前者入门，后者进阶，都有中文版，《代码本色》的英文原版[《THE NATURE OF CODE》](https://natureofcode.com/)还支持免费在线阅读。

从刚开始学 Processing 到现在刚刚入门，The Coding Train 一直伴随着我，常看常新，受益良多。

# Blender 水彩材质-Eevee
![image](https://user-images.githubusercontent.com/20842136/119794251-f28efc80-bf09-11eb-865d-5747a2787e41.png)

Blender Eevee 渲染器实现[水彩材质](https://sinestesia.co/blog/tutorials/watercolor-eevee/)。

# Blender 是怎么免费的？
![image](https://sinestesia.co/wp/wp-content/uploads/2020/10/20180919_145026-1280x720-1.jpg)
[Yes, Blender is free (but what does it really mean?)](https://sinestesia.co/blog/articles/is-blender-free/) 文章介绍了 Blender 是如何做到免费的。

# @motionposters
![image](https://user-images.githubusercontent.com/20842136/119801521-5b797300-bf10-11eb-8a87-0754d1f019d6.png)

[@motionposters](https://www.instagram.com/motionposters/) 是一个创意平台，主要发布动态海报作品。

# 怎样一次做好 99 张封面？
![image](https://user-images.githubusercontent.com/20842136/119796970-67633600-bf0c-11eb-8c61-aefa741ef7d7.png)

[怎样一次做好 99 张封面](https://mp.weixin.qq.com/s?__biz=MzAxOTM5MzY1Ng==&mid=2648610077&idx=1&sn=629c1feda6c7a522e049c5d8346fff97&chksm=83ed880ab49a011c9bcd3a89105997cfd7e597acad1afb9621025199428112d9ca69c832c02e&token=158311053&lang=zh_CN#rd) 详细地介绍了如何批量输出类似封面（主体内容相同，画面中某个元素不断变化）类型的图片。