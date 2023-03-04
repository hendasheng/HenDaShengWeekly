# 很大声周刊-vol.95
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

# Processing to P5js - 留意强、弱类型语言的问题
强、弱类型语言的区别在于定义变量的方式，强类型语言要求在定义变量时就明确其数据类型，弱类型语言，则相反，在定义变量时不要求明确其数据类型。


Processing 基于 Java，是强类型语言。

``` Java
float  f = 1.0;
int  i = 2;
string str = "恰饭和立花"
```

P5js 基于 JavaScript，是弱类型语言（动态类型语言）。
``` JavaScript
let f = 1;
let i = 2;
let str = "恰饭和立花";
```

Processing 和 P5js 的逻辑非常相似，这也是 P5js 开发的初衷，开发者尽可能地使二者能够平滑过渡，但编程语言的限制是不可避免的，就像、弱类型语言这样的问题。

以前多用 Processing，最近更偏向 P5js，主要是它可以跑在网页上。把以前在 Processing 上写好的图形转移到 P5js 时就遇到了上面提到的问题。

``` java
// processing
float f;
println(f); => 0
```
``` js
// P5js (JavaScript )
let f;
console.log(f); => undefined
```

Processing 是强类型语言，变量 f 在声明时就确定它是一个浮点数，默认为 0；而 JavaScript 是弱类型语言，变量 f 在声明时不知道它是啥，默认为 “undefined”。

![image](https://user-images.githubusercontent.com/20842136/222880499-d984ef6b-3e30-4160-bcc2-6ba7d79c495d.png)

同样是变量 f，比如把它用作圆形的半径，在没有赋值的情况下，Processing 就会出现半径为 0 的圆形，而 P5js 中会报错。

在不清楚这一点的前提下，就没办法在 Processing 和 P5js 之间平滑跳跃，如果你遇到了搞不定的问题，可以看看是不是数据类型的问题。

# Cymatics 和 Chladni（克拉尼）
![image](https://user-images.githubusercontent.com/20842136/222877962-c96baec4-46fe-4914-b5ba-4926c234cef1.png)

[Cymatics](https://www.wikiwand.com/en/Cymatics)

> 这类实验类似于伽利略·伽利莱[4]于 1630 年左右和罗伯特·胡克于 1680 年进行的实验，后来由克拉德尼完善，克拉德尼于 1787 年在他的著作Entdeckungen über die Theorie des Klanges（Discoveries on声音理论）。这为理解声学现象和乐器的功能做出了重要贡献。如此获得的图形（借助小提琴弓，沿着覆盖有细沙的光滑板的边缘垂直摩擦）仍然被称为“[Chladni](https://www.wikiwand.com/en/Ernst_Chladni) 图形”。

克拉尼图案应用非常广泛，[Cymatics](https://www.wikiwand.com/en/Cymatics) 页面有更多介绍，最熟悉的应该是 [《指环王：力量之戒》片头](https://www.youtube.com/watch?v=pdjYMSq14ms)。

![image](https://user-images.githubusercontent.com/20842136/222879276-4224edf0-ec52-4392-8435-bb95caa75e97.png)

![image](https://user-images.githubusercontent.com/20842136/222879415-e60a4f7a-bf71-4ee4-bc73-77fc4487e792.png)

[这里](https://www.stashmedia.tv/heres-how-plains-of-yonder-and-nexus-opened-rings-of-power-for-amazon/)简单介绍了创作过程，“Cymatics 是一种自然现象，通过这种现象可以使眼睛看到声音……这是科学和数学，但它会像野性魔法一样打击你”。

## Houdini 实现这种效果
![image](https://user-images.githubusercontent.com/20842136/222879506-ecce0d46-a9a3-4fe7-af07-69e855743080.png)

[《Simulating the Rings of Power Titles - Houdini Cymatics》](https://www.youtube.com/watch?v=_G78lygze8s&list=LL&index=10&t=1053s)

最近一直好奇这种动态是怎么实现的，自己用粒子尝试但搞不定。

[《用houdini制作程序化Chladni图案》](https://www.bilibili.com/video/BV1P94y1o7Aq/?spm_id_from=333.337.search-card.all.click&vd_source=6c68891752436b0097051bf700e169a9) 这里可以完成图案部分。

<img width="1283" alt="283_ChladniPatterns" src="https://user-images.githubusercontent.com/20842136/222879667-a44c7219-b45a-464e-aa1f-683a36fa5416.png">

可动态还是没能解决，可以肯定的是，粒子只在第一帧发射，然后通过力/速度场的设置，影像粒子的位置，如果能把图案转换成力场就好了，可是我不会转。直到发现了 [《Simulating the Rings of Power Titles - Houdini Cymatics》](https://www.youtube.com/watch?v=_G78lygze8s&list=LL&index=10&t=1053s)，手把手教你实现这种效果。

# Houdini - 如何将相机焦点 (DOF) 捕捉到移动物体
<img width="656" alt="65c75ed9bb021b2e776e1bf72f1533e" src="https://user-images.githubusercontent.com/20842136/222770545-01d9855f-77ec-4fbc-bbbc-d657b02ae9be.png">

[Houdini - 如何将相机焦点 (DOF) 捕捉到移动物体](https://vfxbrain.wordpress.com/2020/07/07/camera-auto-focus/)

# 保罗·帕克（图形算法/公式）
![image](https://user-images.githubusercontent.com/20842136/222880154-0967ae5e-9dad-470d-912b-33c733c3e4ec.png)

[保罗·帕克](http://paulbourke.net/geometry/) 列出很多图形的算法公式。

![image](https://user-images.githubusercontent.com/20842136/222880309-511f0a1f-fc04-410c-9d0f-4c74144b97d3.png)

其中还有[克拉尼图案](http://paulbourke.net/geometry/chladni/)的各种形态。

可这都是啥呀，完全看不懂，应该需要很多前置知识吧，现在还属于是看不懂也好看的阶段。

# 小白兔白又白
![微信图片_202303041505312](https://user-images.githubusercontent.com/20842136/222881359-7804c7f8-9584-42a9-a318-9f6413660d91.jpg)
![微信图片_20230304150531](https://user-images.githubusercontent.com/20842136/222881355-59498457-8094-4d68-9686-02f63b8c4b1c.jpg)
![微信图片_202303041505311](https://user-images.githubusercontent.com/20842136/222881358-d13c71b8-dfa5-424e-9638-463fec296a15.jpg)

# 县道184(卷首诗) - 交工乐队
![image](https://user-images.githubusercontent.com/20842136/222880067-ef87383a-d277-4f54-a461-5e3d91f299da.png)
