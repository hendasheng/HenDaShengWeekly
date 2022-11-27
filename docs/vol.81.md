# 很大声周刊-vol.81
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_81](https://user-images.githubusercontent.com/20842136/204139769-92335319-3f2b-4e84-85f3-54e8e4c2448a.png)

# Unicode 大世界 - Processing
![image](https://user-images.githubusercontent.com/20842136/204141141-245a3313-fe0b-4435-ad63-464288d377bd.png)

[Unicode 大世界](https://mp.weixin.qq.com/s?__biz=MzAxOTM5MzY1Ng==&mid=2648609866&idx=1&sn=11399ad2ca169cecdeffead84b7ab218&chksm=83ed895db49a004bd2e788ebcf94513296ae2ac8bd5fb2699dfdb844a5f2fa3bb3aecd8f410d&token=689682383&lang=zh_CN#rd)

> unicode 是一个包含世界上各种语言、符号的集合，你见过的字符、符号，在这里都能找到，每个字符都有与之相对应的唯一编码，这个“编码”就是我们要充分利用的东西。
> 不同语言的字符对应着不同的字符集，字符集就是通过编码来设置，unicode 惯用十六进制编码，比如（"3400", "4DB5" ）代表 CJK 扩展 B 字符集（中日韩扩展 B 字符集），一个 for 循环可以拿到这个字符集中的所有字符，所以你可以通过字符集编码拿到各种字符、符号，可玩性丰富到不行。

# Houdini 输出含多个 uv 信息的 abc 文件
![image](https://user-images.githubusercontent.com/20842136/204143077-f7584035-6ef4-4c83-881f-90667f8229e7.png)

[ROP Alembic Output](https://www.sidefx.com/docs/houdini/nodes/sop/rop_alembic.html) 是 Houdini 中用来输出 [abc 文件](https://www.wikiwand.com/zh-hans/Alembic_(%E8%AE%A1%E7%AE%97%E6%9C%BA%E5%9B%BE%E5%BD%A2%E5%AD%A6))的节点，在包含多个 uv 信息时， `ROP Alembic Output`  默认只能输出一个 uv 信息。

折腾了半天没搞定，搜索一圈发现很多人遇到[同样的问题](https://www.sidefx.com/forum/topic/47927/?page=1#post-377873)，但是并没有能快速解决的办法，想不出办法的时候随便翻着 `ROP Alembic Output`  节点中的设置项，还真发现了解决方法。

![image](https://user-images.githubusercontent.com/20842136/204143478-55541d13-8372-48fc-9658-31b0bd10f344.png)

只需要在 `ROP Alembic Output`  下 `Geometry -> Additional UV Attributes` 中手动填写要输出的 uv 信息即可。

# 更简洁的矩阵写法
![sketch_185_UnicodeToChar_Poster_01_023](https://user-images.githubusercontent.com/20842136/204141384-b9a6f585-054a-443f-8eb4-33470628fedf.png)

通常矩阵需要两层 for 循环，分别在横、纵方向重复。
<img width="800" alt="image" src="https://user-images.githubusercontent.com/20842136/204141488-7cf62a77-2839-4c6a-b530-f7794c2137b0.png">

``` Java
void setup() {
   size(800, 800);
   pixelDensity(2);
   smooth();
   noStroke();
}
void draw() {
   clear();  
   int total = 20;
   float spacing = 44;;
   for(int x = 0; x < total; x++) {
      for(int y = 0; y < total; y++) {
         circle(x*spacing, y*spacing, 30); 
      }
   }
}
```
还有一种更简洁的写法，可以用一个循环完成矩阵。

![ezgif com-gif-maker (21)](https://user-images.githubusercontent.com/20842136/204144870-4843c874-fc3b-4672-90cb-5a8824c87404.gif)

``` Java
void setup() {
  size(600, 600);
  pixelDensity(2);
  smooth();
  noStroke();
}

void draw() {
  clear();

  int total = 207;
  for (int i = 0; i < total; i++) {
    PVector itemSpacing = new PVector(44, 37);
    PVector posOffset = new PVector(43, 38);
    float x = i / 15 * itemSpacing.x + posOffset.x;
    float y = i % 15 * itemSpacing.y + posOffset.y;

    circle(x, y, 30);
  }
}
```
# 小白兔白又白
![微信图片_20221128000410](https://user-images.githubusercontent.com/20842136/204145253-5d99a854-623d-4d24-9998-3861d9d2a561.jpg)
![微信图片_20221128000417](https://user-images.githubusercontent.com/20842136/204145257-2754b095-0cf2-4030-8a49-5d7ce59a0afd.jpg)
![微信图片_20221128000423](https://user-images.githubusercontent.com/20842136/204145258-3591e5d6-27f7-4d91-9332-353b1411a0e5.jpg)

# 后互联网时代的乱弹 第40期
<img width="967" alt="image" src="https://user-images.githubusercontent.com/20842136/204141017-40279672-267d-478c-a2ba-029759219bf6.png">

**[后互联网时代的乱弹 第40期](https://www.bilibili.com/video/BV1gM411k7UF/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# 旅途愉快 - 寸铁
![IMG_1170](https://user-images.githubusercontent.com/20842136/204145250-abe6504f-9017-4811-bf80-731ecafa560a.JPG)
