# 很大声周刊-vol.79
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_79](https://user-images.githubusercontent.com/20842136/201508707-623aea50-9d66-4375-b7a0-48c637c1f0ce.png)

# 模数（取模运算、Modulo）
[取模运算](https://baike.baidu.com/item/%E6%A8%A1%E9%99%A4/4626022)
- 对 2 取模即可判断整数的奇偶性；
- 可用于判断一个数是否能被另一个数整除；

## 对 2 取模即可判断整数的奇偶性
![image](https://user-images.githubusercontent.com/20842136/201511277-02eea2e0-c179-4ddc-aabd-1181a044cb35.png)

画面中有十个方块，在需要对偶数位置的方块进行操作，取模运算就是专门干这个的（不限于）。

## 可用于判断一个数是否能被另一个数整除
![ezgif com-gif-maker (2)](https://user-images.githubusercontent.com/20842136/201511556-6fcad6f3-2c4b-4108-acda-0691c8090012.gif)

当一个数能被另一个数整数时结果为 1（真、true），否则为 0（假、false），
*不同表述方式对应不同场景*

![image](https://user-images.githubusercontent.com/20842136/201511576-d556ce8b-f231-49e6-af82-d96e0dc182e1.png)

图中示意为发射物体，当 `Activation == 1` 时为发射， `Activation == 0` 时停止发射，如果需求是间隔一定时间发射，最直接的办法是通过关键帧完成，但是这个办法操作和调整的成本都很高，这里也可以用到取模运算，可以更高效的完成需求。

比如图中用到 `$FF % 10 == 1`，`$FF` 在 Houdini 中代表帧变量，也可以写作 `$F`，（不同程序会定义不同写法，比如在 Blender 中，帧变量写作 `#frame`）， `$FF % 10 == 1` 指当前帧能被 10 （间隔时间）整除时为 1，否则为 0，也就是通过取模运算控制发射与否，相比手动关键帧来说，这种方式效率更高，调整起来也很方便。

# PolyReduce 2.0 几何节点 - Houdini
![image](https://user-images.githubusercontent.com/20842136/201510063-e3efeb4c-0f8c-4517-a192-57340e7a3d73.png)

[PolyReduce](https://www.sidefx.com/docs/houdini/nodes/sop/polyreduce.html) 减少模型中多边形的数量，同时保持其形状。此节点在缩减期间保留特征、属性、纹理和四边形。

# 上周没搞定的问题解决啦
![image](https://user-images.githubusercontent.com/20842136/201512451-4a062590-4aa7-4652-a23d-79ac08024da0.png)

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/20842136/201512102-66388a44-6503-4a5a-8121-b5a5ed9d5530.gif)

![image](https://user-images.githubusercontent.com/20842136/201512448-a261a243-9012-4f5c-b19a-0bc05e2f65c4.png)

核心是在求解器之前设置不同的 Vellum 压力约束。

![image](https://user-images.githubusercontent.com/20842136/201512498-40e8c09e-4ec3-4b0c-9040-4cb11ae4b7be.png)

在 Vellum 求解器中，单独调整每个压力值。

完整解决方案 -> [在 Vellum 中设置多种压力值](https://www.sidefx.com/forum/topic/87126/?page=1#post-376138)

![image](https://user-images.githubusercontent.com/20842136/201512601-d59ee248-830a-4810-9c7f-70a141acdf6b.png)

现在的解决方案并不是什么窍门或者技巧，它是 [Houdini 19](https://www.sidefx.com/products/whats-new-19/vellum/) 更新的重要功能，我还做过很多相关测试，可能是最近对 VEX 很感兴趣，总是想着用 VEX 解决，反而没想到最简单、直观的方法，这种情况很常见，要小心啊朋友们。

# 小白兔白又白
![微信图片_20221113164301](https://user-images.githubusercontent.com/20842136/201513379-e815e255-dd71-4d4d-90af-ec4d891ee98c.jpg)
![微信图片_202211131643011](https://user-images.githubusercontent.com/20842136/201513382-58ff611c-da20-4650-924b-89ac4f9ec931.jpg)
![微信图片_202211131643012](https://user-images.githubusercontent.com/20842136/201513383-52acd821-d51e-42ef-a3fc-f465cffedbc1.jpg)
![微信图片_202211131643013](https://user-images.githubusercontent.com/20842136/201513384-27e9f382-40b0-4103-b1c8-29236e2f6d0a.jpg)


# 后互联网时代的乱弹 第38期
![image](https://user-images.githubusercontent.com/20842136/201509825-3fb0ea28-3bb5-468c-99c6-f5de8531821f.png)

**[后互联网时代的乱弹 第38期](https://www.bilibili.com/video/BV16G4y1f7hJ/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# Incandescent Structures Of Maybe - Ugress
![9f7a8128e92fb78bec23f29dad6b143](https://user-images.githubusercontent.com/20842136/201509846-729aa0ba-ad1a-4b12-af2c-c3a245fd55ea.jpg)
