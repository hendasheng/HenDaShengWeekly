# 很大声周刊-vol.80
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_80](https://user-images.githubusercontent.com/20842136/202895430-435ea3cf-9a9b-479d-8566-44b6ff3485d4.png)

# Houdini 中 「*」号的应用
<img width="509" alt="3b75a3e0ce57506b17a8c9ad739cf4b" src="https://user-images.githubusercontent.com/20842136/202848983-b16e6978-eaa1-44f6-b919-0e972454de2a.png">

<img width="859" alt="19abb36168f06f15ac936991a02e4c7" src="https://user-images.githubusercontent.com/20842136/202848987-8895cf1b-51ea-4de6-8821-5ff282981d70.png">

选择组时的便捷写法，如在传递组选项中写「group*」，指的是传递所有名称中含「group」的组，在其它操作中也是相同的逻辑。

<img width="728" alt="eca2c3942e090e21826e224505bc733" src="https://user-images.githubusercontent.com/20842136/202848994-88c7c6ab-61f5-46da-9275-1934f067f5ac.png">

在 Houdini 中，「*」多数情况下代表“所有的”。

# 关于贴图资产管理
![image](https://user-images.githubusercontent.com/20842136/202850001-91e7dd6e-e025-4670-a529-47327bf21269.png)

比如类似需求，有一大堆盒子，其中可能包含几类，比如三类吧，但是每个类中的盒子还有差别。

![image](https://user-images.githubusercontent.com/20842136/202849951-92831674-a3db-4731-ad16-fcd171924f8f.png)

这种时候把同类的 uv 放在一张贴图上是个不错的办法，降低贴图资产管理压力的同时提高了效率，也减少了调试成本，特好。

# Entagma - Houdini、Blender 课程
![image](https://user-images.githubusercontent.com/20842136/202851317-5f2ddcc2-cdfe-4806-9f24-e75f8f4fc5a3.png)

> Entagma 主要使用 SideFX Houdini 创建程序设计的高级教程。
>
>由 Manuel Casasola Merkle 和 Moritz Schwind 创立，Entagma 提供深入的教程，主题涵盖生成和程序设计的所有奇怪和美妙的领域。
>
>Manuel 是位于慕尼黑的 3D 设计工作室Aixsponza 的联合创始人。
Moritz是自由职业者 AD/TD/Jack of all tr​​ades，总部位于德国慕尼黑。

[Entagma](https://entagma.com/) 主要出关于 Houdini 相关课程，在 Blender 推出几何节点后，网站中也在更新 Blender 几何节点课程。

Blender 几何节点的逻辑和 Houdini 很相似，在不同软件中跳转会发现会多相同的逻辑，尤其是数学运算，也许操作有差异，但是可以从中获取更底层的新发现。

# 自定义多个颜色（贴图）材质节点 - Blender
![image](https://user-images.githubusercontent.com/20842136/202850264-322d9243-3763-4833-b379-7e75e270a71a.png)

通过「系数」控制不同颜色（贴图）

![image](https://user-images.githubusercontent.com/20842136/202850313-b559778f-3505-4600-872e-a224dfe3caab.png)

![image](https://user-images.githubusercontent.com/20842136/202850507-49889440-4cf1-4680-913e-833fbc1f59b1.png)

核心在于用「映射范围」将输入系数映射到不同颜色上，你可以在此基础上随意增减颜色（贴图）数量，这种方式的好处在于便于管理，并且可以在此基础上再次调整。

![ezgif com-gif-maker (5)](https://user-images.githubusercontent.com/20842136/202850805-28d3d976-bdb4-4c2a-941a-af3c645fa224.gif)

# 得意黑 - oooooohmygosh / atelierAnchor 锚坞
![image](https://user-images.githubusercontent.com/20842136/202894334-aded9936-8a19-4fcb-a8f0-4c4a02592750.png)

[得意黑](https://atelier-anchor.com/typefaces/smiley-sans/)是一款在人文观感和几何特征中寻找视觉平衡的现代窄斜体。

# Houdini 通过颜色拆分物体
![image](https://user-images.githubusercontent.com/20842136/202848692-0421c8b7-dd30-40d2-a76b-520cad06629d.png)

「split」常用于在对多个物体完成统一操作后，需要分别输出，或是需要对每个物体做不同调整的时候，有很多中拆分方法，最近发现一个相对省力的，通过色值区分。

![image](https://user-images.githubusercontent.com/20842136/202848747-73789775-ee59-4fb0-adde-a278b2bc1fa4.png)

没有太多前置操作，先为不同物体设置不同颜色，然后在「split」中就可以用 `@Cd.r==1`、 `@Cd.g==1`、 `@Cd.b==1` 这样的色值表达式拆分不同颜色的物体啦。

# 小白兔白又白
![微信图片_20221119203308](https://user-images.githubusercontent.com/20842136/202851023-6ce40455-ee04-48b9-94e3-c4bfabb7d53b.jpg)
![微信图片_202211192033081](https://user-images.githubusercontent.com/20842136/202851030-59480f1d-b451-431e-a62d-3b7b6f9b6403.jpg)
![微信图片_202211192033082](https://user-images.githubusercontent.com/20842136/202851034-203f2a89-1d64-407e-bd2d-b4ebc006964b.jpg)
![微信图片_202211192033083](https://user-images.githubusercontent.com/20842136/202851035-d2468cd3-0197-4e80-958c-88cf4e1114f0.jpg)
![微信图片_202211192033084](https://user-images.githubusercontent.com/20842136/202851042-bee41949-e18c-47ca-8008-57ea25de281c.jpg)

# 后互联网时代的乱弹 第39期
![image](https://user-images.githubusercontent.com/20842136/202893494-fd9f0c76-02ec-434d-9301-1b6bdc1e9da1.png)

**[后互联网时代的乱弹 第39期](https://www.bilibili.com/video/BV1n3411f7tm/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# Silently - Blonde Redhead
![微信图片_20221119203357](https://user-images.githubusercontent.com/20842136/202851062-97e5cc26-24e7-47c6-9ddb-8e0ea9f40692.jpg)
