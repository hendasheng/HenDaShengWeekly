# 很大声周刊-vol.16
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![118_HenDaSheng-vol-16_01](https://user-images.githubusercontent.com/20842136/130321272-a3130bdc-03fb-4114-b580-86156a37dff0.png)

# Flow Map Painter [Blender]-绘制流动纹理
![3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301](https://user-images.githubusercontent.com/20842136/130320255-3caa9946-8eda-44bb-b8e7-bb0005c089fb.jpg)

由 [Clemens Beute](https://clemensbeute.gumroad.com/#heZDT) 开发的 Blender 插件，在纹理绘制模式下根据自己的需求绘制，就可以产生流动的纹理效果。

[Blender Secrets](https://www.youtube.com/watch?v=0D-dvU6Nt6g) 制作了详细的讲解视频。

本期封面就是通过这种方式完成的。

# 提高 Cycles 渲染速度（Blender）
![image](https://user-images.githubusercontent.com/20842136/130320470-9401ca78-c882-4eef-b714-e4d4878694db.png)

日常多数用 Eevee 渲染，速度飞快，做相对抽象、不那么依赖真实物理环境的场景非常好用，但是遇到需要真实物理光影的场景，还得是 Cycles，最近就频繁用到，看到 [Blender Daily 的介绍](https://www.youtube.com/watch?v=9l_ZptZM2Xs&list=PLSlMI4YOEdKcX8Eex3C4vNp_dI77CQp-1&index=6) ，通过开启渲染设置中的 **“持久数据 (Persistent Data)”**，可以有效加快渲染速度。

![image](https://user-images.githubusercontent.com/20842136/130320490-6b7c50eb-ea2c-4850-80ef-8446586d1018.png)

你一定也想问既然开启“持久数据”就能加快速度，为什么不设置为默认开启？视频下方的评论做了相关说明。

# Blender 形状光束（Cycles）
![image](https://user-images.githubusercontent.com/20842136/130320530-5e0643f5-d6a4-4daa-a5da-3de3a04b919d.png)

依然是 [Blender Daily](https://www.youtube.com/watch?v=ZRSUpr20dj0&list=PLSlMI4YOEdKcX8Eex3C4vNp_dI77CQp-1&index=3&t=5s)，通过给区域光增加纹理的方式，实现形状光束。

# Minim(Processing 音频库)文档
![image](https://user-images.githubusercontent.com/20842136/130320393-d20c8f7e-05a6-4535-82ee-bc959bcd0506.png)

前段时间发过 [Minim 快速入门文档](http://code.compartmental.net/tools/minim/quickstart/?continueFlag=a09723bb3302dd019dd3b52706d0847d)，这份是巨细无遗的 [Minim 完整文档](http://code.compartmental.net/minim/?continueFlag=a09723bb3302dd019dd3b52706d0847d)。

# JSFiddle
![image](https://user-images.githubusercontent.com/20842136/130320736-987fd638-1187-4241-89db-a53b2b506dce.png)
[JSFiddle](https://jsfiddle.net/) 是一款线上调试平台（前端），可以这里编写代码实时查看结果，对我来说最大的用处是可以分享代码，尤其在提问的时候，可以把链接贴出来，对方直接就能运行相关代码，以最快的速度定位问题。

# Stack Overflow
![image](https://user-images.githubusercontent.com/20842136/130320822-db0f4710-88e5-4c6f-b9c3-43e6f4bbfe92.png)

如果你有编程相关的问题，[Stack Overflow](https://stackoverflow.com/company) 是必不可少的好帮手。

# line-clamp
[line-clamp](https://developer.mozilla.org/zh-CN/docs/Web/CSS/-webkit-line-clamp) 是一个 css 属性，可以限制容器中内容的行数。

`
遇到这样一个需求，当窗口宽度大于 500px 时，文本正常显示；当窗口
宽度小于 500px 时，文本要变得短一点，并且在后面加上省略号。
`

第一反应是用 js 实现，试了一下确实可以，但是在响应式的处理上有点[问题](https://jsfiddle.net/niuuin/76L1pszu/10/)，所以就去 [Stack Overflow 上提了问题](https://stackoverflow.com/questions/68871430/js-controls-the-text-length-according-to-the-window-width?noredirect=1#comment121716019_68871430)，很快就收到回复。

![image](https://user-images.githubusercontent.com/20842136/130321041-9da9a2d6-3dfc-4a6f-9de1-87b73b3af6b9.png)

回复中提到 `line-clamp` 这个属性，这还是我第一次听说，果然很好用，只用了 4 行代码就[解决了问题](https://jsfiddle.net/niuuin/1z69k7gy/17/)。

# manoloide
![image](https://user-images.githubusercontent.com/20842136/130321208-96ead268-b198-44c1-8757-e42fe287dea6.png)
前几期内容中介绍过 [manoloide](https://www.behance.net/manoloide)，主要想说的是他的更新频率太吓人了。