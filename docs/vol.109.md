# 很大声周刊-vol.109
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_109 1](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/4ec21291-1229-47c2-b261-eaaed16fd070)

# Houdini Vex 累加 - 求解器
![ezgif com-video-to-gif (5)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/16ab4910-f901-4c89-83dd-84071cd3597b)

``` C
int num = 0;
if(@Frame % 30 == 0) num++;
```

上方的运算逻辑很简单，每过 30 帧，为变量 num 加 1。不过在具体执行过程中会遇到程序运行流程的问题。

需求中说了两件事：
1. 创建 num;
2. 每过 30 帧，为变量 num 加 1;

第一条只在开始的时候运行一次，第二条则是循环运行。如果不考虑这一点就会出现这样的问题。

![ezgif com-video-to-gif (7)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/a7793cf4-1d9e-411b-9645-2b14881a1f4e)

``` C
int num = 0;
if(@Frame % 30 == 0) num++;
```

这里的 1 和 2 一样，一直在循环运行，所以每次 num 在加 1 之前都会被归零，也就不能实现希望中的累加。

用 P5js 举例看会更加直观，P5js 中有两个基础函数 `setup()` 、`draw()`，前者只在程序开始时运行一次，后者则是循环运行。

![ezgif com-video-to-gif (8)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2b5489fb-d6d0-431a-be8f-8ab47e66b0be)

把 1、2 全部写在 `draw()` 就重现了刚刚提到的问题，每次 num 加 1 前，会被归零，因为两条需求都在循环运行。如果把 1 写到只在开始时运行一次的 `setup()` 中，就可以实现希望的累加效果。

![ezgif com-video-to-gif (9)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/438d8271-6f9b-47d7-ac19-318597cea3fb)


## Housini Solver
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/f6efa6df-5594-48f2-85b7-cf26c408edde)

Houdini 也对这样的需求有相应准备，不过文档中的描述更偏向 3d 语境。

一定程度上可以粗暴的把 [Solver](https://www.sidefx.com/docs/houdini/nodes/sop/solver.html) 理解成 P5js 的 `draw()`，反正它可以循环运行。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ebb5ab68-0eed-4740-a0f7-9f61cc481455)

- 这样就可以在 Solver 外部定义 num 变量

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1cf132f5-b2ad-466e-87fc-8272cd27d86b)

- 在内部循环运行 num 加 1


![ezgif com-video-to-gif (5)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/16ab4910-f901-4c89-83dd-84071cd3597b)

这样就用和 P5js 同样的原理，或者和大多数编程语言同样的原理，实现了累加效果。

# Houdini 获取自定义变量 - 程序化建模
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3bbdd645-cb9a-4958-a336-6cbcd0ede94c)

如果想通过线条长度控制圆形挤出高度怎么办？

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d45a56d2-b749-4d81-827c-fd051e3aedec)

最简单的办法是直接把线条 `length` 复制到 `distance` 上，但是这种方式不能面对复杂场景，很多时候没有现成的 `length` 可以直接拿来用，所以需要更彻底的方式来完成这件事。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cf17cca3-08f9-44c2-8865-9df922903733)

首先通过计算拿到线条最高点的位置 `distance`，并将这个参数传递给需要挤出的圆环。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/8f21be3f-39df-4f8d-9046-81e19c0bf13c)

如果在 `polyextrude` 中直接引用 `distance`，会出现报错，程序不允许这样直接引用，所以需要通过 `attribpromote` 进行转换。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/4afaea5a-82e6-4caa-bc8c-9c5ba6629998)

将 `distance` 从 `point` 转换为 `Detail`，我现在还没有能力解释清楚这件事，但本质上就是数据类型转换。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ebb0bca7-534a-405a-bbaa-84c0b5e6e640)

转换后通过 [detail()](https://www.sidefx.com/docs/houdini/expressions/detail.html) 函数引用 `distance`。

![ezgif com-video-to-gif (10)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/74e56cad-c283-44f7-a96a-888883fa6d64)

这样就完成了开头的需求，看起来好像是把简单问题复杂化，但这种方式在程序化建模中非常重要，几乎可以让你引用一切属性，用尽可能简洁的方式做控制项。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cd641f1f-fe01-46a9-8f50-deb22db05b6e)

前面关于累加的实例，为了看起来更直观，也用到了这种方式。

# 小白兔白又白
![微信图片_202306111726422](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3ec14748-1e18-4f14-81b3-9f7ae71e1303)
![微信图片_202306111726423](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/8ca24c93-4406-4bbc-94dc-4c5ab06e7bd8)
![微信图片_20230611172642](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/972b09cb-21e7-445c-a958-54a46073e669)
![微信图片_202306111726421](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/60f3f7af-0e4e-477c-9454-9698ec6f9a12)


# 破了洞的美梦 ( Taipei Ocean ) - 伤心欲绝
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d2134a89-1c35-4dd3-bb6f-0c7742498e8d)
