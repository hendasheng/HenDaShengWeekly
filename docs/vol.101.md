# 很大声周刊-vol.101
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_101 1](https://user-images.githubusercontent.com/20842136/232326761-03919fe0-ae98-48ce-8a54-9644df0a9fea.png)

# Houdini FBX 文件批量输出的问题
## 通过 For 循环输出每个部分
![image](https://user-images.githubusercontent.com/20842136/232292834-89627fc1-cf54-49ef-9ef7-cc866d4abfe1.png)

最初想到的是通过循环批量输出，各种连线方式和表达式写法折腾了好几天，最终在[《Python in Houdini 1 : Batch Exports with "For Loops"》](https://www.artstation.com/blogs/b00merang/Mgrq/python-in-houdini-1-batch-exports-with-for-loops)这里找了解决方案，通过文本和图片的方式说明了原理和用法，我在 Houdini 论坛中做了一份[示例文件](https://www.sidefx.com/forum/topic/89701/?page=1#post-390043)，可以更方便的理解整个逻辑。


## ROP FBX Output 节点 path 属性
![image](https://user-images.githubusercontent.com/20842136/232294039-0fe36be4-a6f8-4737-9207-ecf4d2ba380d.png)

![image](https://user-images.githubusercontent.com/20842136/232294206-57967237-d212-4670-bf35-27301217cc8b.png)

这是更简单的方式，打开 [ROP FBX Output](https://www.sidefx.com/docs/houdini/nodes/top/ropfbx.html) 路径属性，给每个需要单独保存的部分创建 `path ` 属性，属性值则是这部分的名称。

![image](https://user-images.githubusercontent.com/20842136/232294757-76314b85-142b-4bde-aa7c-b1cc5c5930e1.png)

---
两种方式针对不同需求，前者会为每个部分单独创建 `.fbx` 文件，后者会将所有部分打包在一份文件内。

# Houdini 两种删除点/线/面的方式
[removepoint](https://www.sidefx.com/docs/houdini/vex/functions/removepoint.html) 和 [blast](https://www.sidefx.com/docs/houdini/nodes/sop/blast.html) 两种方式都可以做到删除。

**removepoint**
![ezgif com-video-to-gif (1)](https://user-images.githubusercontent.com/20842136/232297885-925105b6-82be-47c8-b4fc-3c34e90d2cce.gif)

在实际过程中发现这种方式在大多数情况下都没问题，可能遇到的问题是，后续做复杂处理时可能会识别错误，我也不知道为啥，但是可以通过 removepoint + blast 的方式解决。

![ezgif com-video-to-gif (2)](https://user-images.githubusercontent.com/20842136/232298659-4a2c2fb2-f797-4075-876c-b52cc15b585b.gif)

先选择需要删除的部分，保存导组中，再用 blast 删除这个组即可，反正可以解决识别错误的问题，等我知道具体原因后再聊其它的。

# UE 导入模型时提示 「ue 无法三角剖分网格」- Houdini
![image](https://user-images.githubusercontent.com/20842136/232299828-d19aa4a1-44c2-47b8-b339-e40a8c8a8cd0.png)

可以在导出前用 [Divide](https://www.sidefx.com/docs/houdini/nodes/sop/divide.html) 处理模型，它可以修复多边形，将 N 边形划分为三角形或四边形，修复后可以正常导入 UE。

# 小白兔白又白
![微信图片_202304161817142](https://user-images.githubusercontent.com/20842136/232295228-ca06301d-579e-48ee-983c-1ca1cb80d494.jpg)
![微信图片_20230416181714](https://user-images.githubusercontent.com/20842136/232295240-6399855c-70ff-4483-a1c4-54a687f588e6.jpg)
![微信图片_202304161817141](https://user-images.githubusercontent.com/20842136/232295246-62177f4e-e639-4ea3-9a89-395f3af03fd4.jpg)

# 床 - 草东没有派对
![image](https://user-images.githubusercontent.com/20842136/232326846-e94b8ff8-6b40-4a7f-97f7-ad38d5b9fc0f.png)
