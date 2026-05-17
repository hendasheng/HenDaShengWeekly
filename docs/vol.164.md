# 很大声周刊-vol.164 Houdini 有意思

# p5js 动态数据引入 Houdini
突发奇想的流程，试了一下还真给跑通了。

我用 p5js 做过很多点动画片段，算法驱动的动画很多时候会有惊喜，不同的参数搭配总是能带来意想不到的反应，这一点很吸引我，但是 p5js / processing 这类工具并不擅长光影和更复杂的处理，拿到 Houdini 里面正合适。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/p5_SpherePoints.png)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_SpherePoints.png)

因为不同的动画需要针对性的处理，这里只聊思路，具体代码在当前 AI 的能力下很容易处理，就算是这个流程的 Skill 吧。

P5js json 2 Houdini：
- P5js
    - 写好动态；
    - 将点数据导出为 JSON； 
- Houdini
    - Python 读取/解析 JSON；
    - VEX 继续处理点属性；
    - 最后复制到点 / 实例 / 渲染；

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_SpherePoints_01.png)

这是基本的流程，在 Houdini 中解析 JSON 之后，后面还有巨大的拓展空间，可以根据实际需求做任意调整。

# Houdini Cops 图像到网格模型
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_cops.png) 

[Houdini Cops](https://www.sidefx.com/docs/houdini/copernicus/intro.html) 是处理 2D 图像数据的节点网络，从 Houdini 20.5 开始做了大的更新，可以和 SOP（3d）数据互通，它的用途非常广泛，最近我在处理非常规图形建模时用到了它。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_cops_img2mesh.png)

图像的灰度信息可以直接影响点位置、网格高度、密度分布等等数据。这和渲染器里的凹凸、置换有着本质差异。渲染器的处理方式很聪明，对性能非常友好，但也存在很多限制。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_cops_img2mesh_01.png)

而在 COPs 到 SOP 的流程里，图像灰度可以直接参与几何生成，变成真实的点位置和网格高度，这就给后续的步骤留出足够的操作空间。

# Houdini 获取 SOP Detail 属性的两种方法
## 路径引用
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_get_detail_01.png)

## 索引引用
增加 Spare Input，输入目标节点，vex 中就可以通过索引的方式引入对应属性。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/houdini_get_detail_02.png)

# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/IMG_1812.jpeg?x-oss-process=image/quality,q_50)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/IMG_1877.jpeg?x-oss-process=image/quality,q_50)

# Falling out of Love - The Strokes
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.164/Falling%20out%20of%20Love-The%20Strokes.jpg)