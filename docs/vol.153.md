# 很大声周刊-vol.153
![Title_WeChat_153](https://github.com/user-attachments/assets/a2392551-423c-4d3c-ad51-8222f00073cb)

# 关于 241019 开发片段
![HighresScreenshot00000](https://github.com/user-attachments/assets/d809147d-940a-4ce0-93fa-b16f80a5aa7b)

241019 开发片段在干嘛、为什么没搞定、接下来咋整。

![容器 31@1x (1)](https://github.com/user-attachments/assets/6951e3ca-5e9a-4db3-a0f1-aff2443708df)

来源是夏天在公园拍的照片，下雨天，正是雨停下来的间隙，路灯把树照的很好看，夏天可太好了。

我想复现这个场景用来演节目，希望是有画面、有声音、有联动，结果从夏天拖到秋天，也不完全算拖吧，期间在逐步解决一些问题，顺便也试一下不同的工具，到现在还没整完。

![HighresScreenshot00001](https://github.com/user-attachments/assets/a2bbf4de-d253-4844-a76b-304501bba773)

## 场景复现
目前只实现了一个镜头，整体还是在 UE 中完成，路灯建模部分通过 [Houdini Engine](https://www.sidefx.com/products/houdini-engine/plug-ins/unreal-plug-in/)，它可以联通 Houdini 和 UE，可以直接在 UE 中调整定义好的参数，相比常规的导出导入，这种方式更灵活也更高效，尤其是方便调整。

游戏引擎或者实时渲染引擎对我来说最大的感受是会用各种匪夷所思的方式来解决问题，为了实时且高质量会好多很聪明的办法，以前更多使用离线渲染，最大的差异就是渲染质量，离线渲染质量高的成本是更长的渲染时间，实时渲染就是字面意思，渲染质量会低一些，这里的“渲染质量”是相对概念，抛开这些概念讲，目前实时渲染的渲染质量是可接受的，非常可接受。

![image](https://github.com/user-attachments/assets/e6bdd921-e13c-4423-ac42-902dfe007b00)

树的部分用到 [UE - Megascans树木：欧洲桤木（抢先体验）
](https://www.unrealengine.com/marketplace/zh-CN/product/megascans-trees-european-black-alder-early-access)。

![image](https://github.com/user-attachments/assets/3dae25bc-3d64-4b26-bdb6-8e37ba47fa44)

它是商店里的资源包，做的特好，提供大量的控制接口，可以调整季节、风速、风向等等参数，测试中从夏天过渡到秋天就是在发现它可以控制季节才想到的，我做东西一半是灵感驱动，另一半是测试驱动。

既然提供可控制接口，那接口就应该可以作为交互控制项，这里有一点麻烦，如果只是在界面中调整这些参数会很简答，想要它在某些情况下被触发就需要一些逻辑上的设定。

![image](https://github.com/user-attachments/assets/65d4bfa4-228a-48d3-9f09-fac3429f4468)

想要完成在某些情况下触发需要一定的前置知识（对蓝图有一定了解，知道如何实现自定义函数），文件中的 `BP_GlobalFoliageActor_UE5` 就是干这的。

![image](https://github.com/user-attachments/assets/42b087f5-3ff5-4e81-9c1d-a4ba4c553371)

打开它会发现可控项就在其中，是一个个设定好的变量，只需要根据需求完成控制逻辑就好。

变量就是可控项，可控项就是变量。只是语境不同，在编程中称为“变量”，在应用中成为“可控项”。

## 声音部分
声音部分还没做好，憋了好几回憋不出来，我再想想办法。

## 后面要更新的
目前只有一个镜头，我想做更大的世界，一方面是这样会有更丰富的视觉体验，另一方面需要它支撑整段音乐。

最近了解到 UE 推出的 [PCG（Procedural Content Generation - 程序化内容生成）](https://dev.epicgames.com/documentation/en-us/unreal-engine/procedural-content-generation-overview) 。

> 在 Unreal Engine（UE） 中，Procedural Content Generation (PCG) 是一种利用算法或规则动态生成内容的技术。PCG 能够在不需要手动创建的情况下，通过程序控制生成海量的游戏元素，如地形、环境、建筑物、物体分布，甚至可以用来生成关卡或复杂的任务系统。

直指目前的痛点，不过这些工具得试一下才知道，先试试看吧。

后面大方向基本就是这样，视觉上的大世界和完整的音乐，再稍微练练琴，弹的也太差了。

# 小白兔白又白
![微信图片_20241020170304](https://github.com/user-attachments/assets/9bc9a285-06f2-4456-9bfe-f9c20ed6b9d2)

# 爱情的大坏蛋 - 美秀集团
![image](https://github.com/user-attachments/assets/0a8b4cbb-c080-4296-a95a-25dbbf06dcd0)