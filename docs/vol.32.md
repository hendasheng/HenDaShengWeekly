# 很大声周刊-vol.32
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![sketch_172_HenDaShengWeekly_vol-32_01_1221](https://user-images.githubusercontent.com/20842136/145701569-94e3e78f-72e1-4a39-ad34-d0f46acb6e7f.png)

# 文本动态点线实验
![image](https://user-images.githubusercontent.com/20842136/145701818-9af3cf0b-6bbb-4f5a-8a9b-7580489dbf7b.png)

![image](https://user-images.githubusercontent.com/20842136/145701884-147d8341-84f0-4639-9a6a-42599acb9689.png)

![image](https://user-images.githubusercontent.com/20842136/145701913-0c6d9afd-d81e-47d5-8eee-a52d9ba3677d.png)

![image](https://user-images.githubusercontent.com/20842136/145701988-5919bdef-a124-4c82-ba3c-e0a21a6baa2b.png)

>  **[文本动态点线实验](https://www.behance.net/gallery/132642449/Text-to-points-line-experiment)** <br>
提取文字轮廓点，叠加多个层级，并为这些点设置不同运动规则，在运动过程中可以让原本相同位置的点处于不同位置，这样就有了线，点与线在画面中游走、交错形成了最终的形态。这是我关于字体样式的实验，希望你喜欢：）

p5js 和 processing 在功能和逻辑上基本相同，但是基于不同底层语言的原因，多少会有些差异，[textToPoints()](https://p5js.org/zh-Hans/reference/#/p5.Font/textToPoints) 就是其中一点，它可以计算文本轮廓，并生成点数组，这在 [Procesing](https://processing.org/) 上就不太容易实现，如果想实现类似效果，需要借助 [Geomerative](http://www.ricardmarxer.com/geomerative/) 完成。

我在这这组作品中主要用到的就是 [textToPoints()](https://p5js.org/zh-Hans/reference/#/p5.Font/textToPoints) ，通过它生成文本轮廓点数组，在此基础上进行动态和图形化的尝试。

# Google Fonts
![image](https://user-images.githubusercontent.com/20842136/145702086-99dc841c-d74f-44f4-9172-d99191026d68.png)

[Google Fonts](https://fonts.google.com/) 是一个包含 1,333 个免费许可字体系列和 API 的库，可通过 CSS 和 Android 方便地使用。该库还为常见的操作和项目提供了令人愉快且制作精美的图标。下载它们以用于您的 Android、iOS 和 Web 数字产品。

# 在 P5js 中通过链接的形式引入 Google Fonts
![image](https://user-images.githubusercontent.com/20842136/145702071-90e62917-7e72-4576-a2f2-0da1712feb51.png)

在 P5js 中通过链接的方式引入 GoogleFonts 字体。常规引入方式是把字体下载到本地，再通过预加载引入，整个过程很麻烦，想更换调试字体就又得把整个过程重复一遍。通过链接的方式无论引入还是更换字体都会更便捷。

1. 在 GoogleFonts 中选择需要的字体，可多选；
![image](https://user-images.githubusercontent.com/20842136/145702286-ea856a60-7087-4f37-a6c1-a6bc3bde7231.png)


2. 显示已选择字体并复制 link 标签；
![image](https://user-images.githubusercontent.com/20842136/145702293-50a85da8-824a-458a-82f8-30e76ae97f8b.png)


3. 粘贴到 html <head> 中；
![image](https://user-images.githubusercontent.com/20842136/145702295-ca9e91f7-083d-4e75-a02d-4485393781ee.png)


4. 复制 <link> 标签中 family 的值，在 P5js 中设置字体。
![image](https://user-images.githubusercontent.com/20842136/145702297-9c50360d-116c-4fa4-96a5-4dd7bfc35f13.png)
注：“family=Dela+Gothic+One” 中间的 “+”，在 P5js 中等于“空格” textFont("Dela Gothic One")。"

[P5js 引入 GoogleFonts 字体 - 测试代码](https://editor.p5js.org/niu/sketches/UUwHi7ufK)

# Blender 3.0 几何节点 - Fields

Fields 是 Blender 3.0 几何节点的核心概念，理解起来并不容易，跟着实际案例，在实际操作过程中慢慢理解，或许是不错的办法。

## Blender3D 3.0 - Procedural Flower 
![image](https://user-images.githubusercontent.com/20842136/145702799-3a05e9ea-8f64-4c86-9122-f1ad894de34a.png)
[《Blender3D 3.0 - Procedural Flower》](https://www.youtube.com/watch?v=Qj3M58GFXrw)

## Blender Geometry Nodes 3.0 - Plant Growth with Fields
![image](https://user-images.githubusercontent.com/20842136/145702873-63ded439-8d89-4de9-abd0-25e2cd2ffb81.png)
[《Blender Geometry Nodes 3.0 - Plant Growth with Fields》](https://www.youtube.com/watch?v=XSkaM-8Vgz8)

## Blender 3.0 Beginner Geometry Nodes Tutorial
![image](https://user-images.githubusercontent.com/20842136/145702904-c4d0ddaf-07a9-4d93-bd43-dcb837951fce.png)
[《Blender 3.0 Beginner Geometry Nodes Tutorial》](https://www.youtube.com/watch?v=uslTaqiv_7k)

# 《毛骗》十年，走不出的石家庄
![p2655812779](https://user-images.githubusercontent.com/20842136/145702627-fe00b180-1285-4759-8bb5-6435b4e0de9d.png)

[《毛骗》](https://movie.douban.com/subject/26603847/) 应该是最早的网络剧集了吧，现在看画面并不精致，但内容质量依然精彩。[《毛骗》十年，走不出的石家庄](https://mp.weixin.qq.com/s/crBNb1pCSMaRAHEai3ZdXQ) 这篇文章介绍了主创和他们的近况。

# KID A MNESIA - RedioHead 新专辑
![download](https://user-images.githubusercontent.com/20842136/145702271-268761c0-096e-44a4-88cd-bd0530fe1b21.jpg)

> 如同一贯难于被定义的多变乐风，这张拥抱电子音乐的《Kid A》再次带来惊艳。Radiohead 继续自我进化，带我们跌入新的幻想境地。专辑以“冷酷仙境”般的电子氛围回环缭绕，不变的依然是乐队“恍如隔世”一般的氛围打造，与 Thom Yorke “看淡人间烟火”般的飘渺嗓音。大胆融合体现后现代主义的艺术概念，专辑中合成器、管弦配乐与鼓机大行其道，将电子、氛围、爵士以及二十世纪交响乐精巧融合。开篇曲《Everything in Its Right Place》用厚重的合成器声效与 Yorke 处理过后的破碎人声，预示着乐队风格大刀阔斧的改变；受到自由爵士影响的《The National Anthem》中，铜管乐器“肆无忌惮”地撕扯着整首歌的框架，呈现出自由癫狂状态。《Kid A》虽然听起来已经不像是一支摇滚乐队的专辑，但可以很容易感受到的是，这就是 Radiohead。 - Apple Music