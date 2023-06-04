# 很大声周刊-vol.108
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_108](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0748fd3e-7a02-49e3-9a7f-8bc49e08e368)

#  画一个圆 - 弧度值问题
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/869eda17-1d0c-4dbd-8c77-cb6c4f9e91a1)
<!-- <center><font color="#888">P5js<font></center> -->

在[极坐标系](https://www.wikiwand.com/zh/%E6%9E%81%E5%9D%90%E6%A0%87%E7%B3%BB)下可以通过：
```
x = sin(theta) * radius;
y = cos(theta) * radius;
```
这组公式绘制圆形。

图中的点虽然组成了圆形，但是看起来乱乱的。原因在于极坐标中采用的是弧度值单位，循环中 i 代表每次循环的弧度增量，可是目前 i 并不是弧度，需要通过 radians() 转换，这样就可以让点均匀分布在圆形上。

``` js
for (let i = 0; i < 360; i++) {
    let x = sin(radians(i)) * radius;
    let y = cos(radians(i)) * radius;
    point(x, y);
  }
```

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/75f251a5-bfe0-4193-af83-716222054d07)

多数需求应该是需要自定义点数量，那就需要提前做好弧度值转换：

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/e71f7fcd-e38f-45b1-ad59-f1d663490d9a)

通过这种方式可以用任何趁手的工具绘制圆形：

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/aadb7a05-0224-41dc-9fb0-ef57eb597d9a)
Blender 几何节点

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ddf11bab-6e3c-41a6-91ef-bc6b67d194d9)
Houdini Vex

## 点到线
如果不注意弧度的问题，将点连接成线的时候会出现很奇怪的问题：

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1086cd41-718a-4bc4-8a21-f028e3ca4635)
P5js

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/5d05383e-2141-4c1d-ac75-08589b5bdaec)
Blender 几何节点

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2e8a1292-e34d-4224-ac0f-8af711303d73)
Houdini VEX

有些时候 Bug 会带来奇妙效果，但在只想老老实实画个圆的时候，就会很头疼。

上面三种环境的连线逻辑都是相同的 —— 根据点编号依次连接。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/117fa982-622d-4803-aafa-60b1bd48441b)

就像开头提到“点看起来乱乱的”，不做弧度值转换的结果是点编号错乱（或者说不是按照希望的样子排列），连线的时候自然也乱起来。

如果是像圆这样的基础图形还好，可能会有其它解决方法，但面对通过点计算方式完成的复杂曲线，千万要留意弧度值的问题啊。

# Houdini Engine - Unreal
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/94308aab-5b72-430d-962f-10c42a6f2a9c)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1f861d24-2ffb-4629-be70-53b9742ca192)

除了程序化建模之外，在 Houdini 中的物理模拟也可以通过这种方式导入 UE，这里指的是模拟结果的静态导入，已知可以导入动态的是 RBD 模拟，其它的模拟还不清楚。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/05277bbf-192f-4063-9c0e-98900ac8f836)

[Houdini 到 UE 的程序化资产](https://www.sidefx.com/tutorials/foundations-procedural-assets-for-unreal/) 基础使用演示。

# Unity 支持直接导入 blender 文件
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/32eb2b39-61f6-4d72-93be-58efeec8f2b2)
[Unity 支持直接导入 blender 文件](https://unity.com/how-to/beginner/using-blender-and-maya-unity#seamless-importing-unity
)
> 必须转换第三方项目文件才能将它们用于其他应用程序非常耗时。它也可能不可靠，即使是承诺兼容性的软件产品也是如此。但是使用 Unity 从 Blender 和 Maya 本地导入项目文件很容易。
>
> 要将 Blender 资产导入 Unity，请单击 Unity 菜单栏上的资产 > 导入新资产，然后找到并打开您的 .blend 文件。
>
> 要在 Unity 中使用 Maya 文件，请单击 Unity 菜单栏上的 Assets > Import New Asset，然后查找并打开 Maya 的 .fbx 文件。

感觉 Unity 导入资产相对麻烦一点，通过 Blender 文件导入会方便很多，相当于在 Blender 做好整合，再拿到 Unity 中。

# 小白兔白又白
![微信图片_202306031837141](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/f73d239d-e3fc-4f45-a882-2b80b2e0ff98)
![微信图片_202306031837143](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/13c3a7c7-67f1-4071-bd07-95d0fbb712ec)
![微信图片_202306031837142](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3aec7b66-17ba-4d36-ace1-11ac510e929d)
![微信图片_20230603183714](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/5135e13b-8d84-492e-8077-e2e027fd50d8)
![微信图片_202306031837144](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/9953eb83-cfb5-4565-91cd-e554d73f0212)

# そして僕は途方に暮れる (feat. 黒川沙良)
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/499f051a-b41c-4ab4-a614-83e06387ce3e)
