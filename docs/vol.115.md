# 很大声周刊-vol.115
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

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


