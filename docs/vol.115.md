# 很大声周刊-vol.115
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_115](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/532699ed-2134-414f-ac0e-ec710bb9d514)

# 提取中心点 - extract centro id - Houdini
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c5efa491-5972-44b4-856e-99281e6e18ff)

[Extract Centroid](https://www.sidefx.com/docs/houdini/nodes/sop/extractcentroid.html)

发现这个节点前通常会这样做：

- 先用循环找到每一块
- ![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/81c55208-917f-4c4b-ba2a-1273f81f5f21)
- 在每一块的中心位置创建点 `$CEX $CEY $CEZ`
- ![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/66c682ef-e769-4221-95b3-778d349921bb)
- 通过 `@ptnum - 1` 找到最大值（新增点的编号），并删除其它点。
- ![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/72698210-fea7-47e2-8922-9e8b1b844995)

这样就找到了每一块的中心点。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2e2c97a2-08c0-4ccd-8d12-099e110415bb)

这种方式或许可以帮助你熟悉一些 Houdini 内置脚本写法，虽然过程也不算很复杂，但有些情况下中心点找的不是很准。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/dd64e338-93c0-44e5-a70b-c3df5a795d0b)

直到发现了 [Extract Centroid](https://www.sidefx.com/docs/houdini/nodes/sop/extractcentroid.html) 这个节点，它用最短平快的方式解决了类似需求。

# 点编号（@ptnum）与点总数（@numpt）
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/09725c97-a85f-44f0-ab20-1eb3832344fb)

``` C++
// 点编号
@point_num = @ptnum;
// 点总量
i@point_total = @numpt;
```

# 面编号（@primnum）与面总数（@numprim）
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ff89fb0d-8d44-43a3-a381-d07c3c7f9a17)
`@primnum` - 获取面编号

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/14bcb98a-6bd3-4264-8614-bb8411664db1)
`@numprim` - 获取面总数

用「面」来形容并不严谨，不过大概就是那么个意思。

获取 `point / primitive` 的编号、数量属性的逻辑相同， 其它属性应该也是类似吧。

# Constraint Simple Blend(Chop) - Houdini
 ![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0d91d19e-cf3d-4d57-aa48-6478d2353144)

[Constraint Simple Blend(Chop) ](https://www.sidefx.com/docs/houdini/nodes/chop/constraintsimpleblend.html) 节点用来混合相机非常好用。

![ezgif com-optimize (2)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/6963f8ea-5b10-4d38-8add-e76154601603)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/4139d369-8d6d-432e-85d4-ad1f0362f4f6)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2716525a-0101-4774-ab3b-fb34596e7ffc)

它有自由度很高的可控项，常规做法应该就是混合多个相机的位置/旋转信息，用最终输出的相机（图中 cam_mix）设置景深、焦段等等其它信息。

# SideFX Houdini : Action Sequence Design - Adrien Lambert
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2741cc9f-50f8-4733-ac54-5e8a7f7a94df)

[SideFX Houdini : Action Sequence Design - Adrien Lambert](https://www.youtube.com/watch?v=osNHbZIwU-Y&t=734s)

在这里学到很多关于相机的知识。


# 小白兔白又白
![微信图片_20230723210740](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/6e7937de-3759-49a0-b9fd-937f6bc1a614)
![微信图片_20230723210742](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3a0ebad0-b535-46e9-bab2-cde618f06b31)
![微信图片_20230723210743](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1b2ca359-c1f7-40bd-af08-267eb34ef2da)
![微信图片_20230723210741](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3109e229-05ac-4e6e-a33f-eeae807f4ed9)

# Abrasive - Ratatat
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2b768bd9-76a7-400f-8a83-022c28b21ef7)