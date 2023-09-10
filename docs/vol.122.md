# 很大声周刊-vol.122
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_122](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/a1cb94d8-ae0a-4785-8f81-8d1554edc966)

# Houdini Copy To Points - 循环控制变量
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/58bfc922-929a-4db8-ba15-cbbdee386daf)

上期聊到通过手动增加 name 属性，将多个物体分布到点上，这种方式多数情况下是管用的。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/15028de5-d350-4e45-931c-583f3286d4ea)

可是想把被拆分成 100 块的石头，和另外一些多边形同时使用时就不能手动操作了，这种情况就是循环最擅长的事。

这里指的 [循环](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/Building_blocks/Looping_code) 是编程中的概念，和字面意思一样，在特定条件下重复做某些事情。不止是 Houdini，任何编程沾边的环境下都是这样。

比如示例中，被拆分成 100 块的石头，和 3 个多边形，总共 103 个物体。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/bfdfb8ef-8791-47bb-b436-4fe8162ea222)

循环有一个很重要的特性是它的迭代值，是一个变量，它代表循环的次数，在当前需求下，正好可以用它来给每个物体命名。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/bba64a4f-8916-4bff-a554-cbab3a5eface)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/263049d4-7c86-4f00-870b-d0f450545190)

这里创建了整数 variant 属性，属性值就是循环中的迭代值（示例中的写法是 Houdini 中定义的写法，不同编程环境写法会有差异，但逻辑完全相同），顺便还给每个物体创建了 UV。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/34064892-ada0-4b14-ab02-e67aa46536b7)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/da9e4b8b-60f9-4691-a0f5-a9f7c9fe26e8)

接下来再通过刚刚定义好的 variant 属性将物体复制到点上。

--- 

做示例的过程中发现，不用循环也行，通过 [Connectivity ](https://www.sidefx.com/docs/houdini/nodes/sop/connectivity.html) 节点
的 class 属性也可以做到，循环的重点在于分别对每个物体进行操作，比如示例中给每个物体创建 UV，就必须要通过循环才能完成。

# 小白兔白又白
![微信图片_20230910153226](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/f86645f6-e391-4931-809f-7b9f17de5063)

![微信图片_20230910153227](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/166c9ae5-7f2a-4840-830f-c69c4d5e847f)

# The Rime - SCSI-9
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/41818b5e-a808-43b5-adf1-4459dbcd5b3d)
