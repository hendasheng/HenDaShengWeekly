# 很大声周刊-vol.08
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![93_HenDaShengWeekly-08_03_](https://user-images.githubusercontent.com/20842136/123507439-ef6b6580-d69b-11eb-95ba-7eb3c82942cb.png)

# 种下这支花，忘了那个她
![IMG_7933](https://user-images.githubusercontent.com/20842136/123507422-ce0a7980-d69b-11eb-98ee-64d9863863af.jpeg)
<p align="center">第三周</p>

![sketch_115_PolarPerlinFlower_01_92](https://user-images.githubusercontent.com/20842136/123508803-2e9db480-d6a4-11eb-8c33-5365e9e4c1ea.png)

# Blender 程序化纹理

## Erindale
![image](https://user-images.githubusercontent.com/20842136/123507749-b9c77c00-d69d-11eb-9d7c-f2efb8b6e14f.png)

![image](https://user-images.githubusercontent.com/20842136/123507781-f8f5cd00-d69d-11eb-9e5f-fb1e053d5927.png)

就是制作 Blender 2.93 封面图的 [Erindale](https://www.youtube.com/channel/UCGMyyn2FdEFcDfP1wQRh5lQ)，他用程序纹理做出很多看起来匪夷所思的事情，用到的节点量非常吓人。

## Sam Bowman
![image](https://user-images.githubusercontent.com/20842136/123507840-55f18300-d69e-11eb-895a-cdfd7e24a20d.png)

![image](https://user-images.githubusercontent.com/20842136/123507870-a9fc6780-d69e-11eb-82d1-8c9de521e823.png)

在 [Sam Bowman](https://www.youtube.com/channel/UCbODs2qqHISelcvKZybRMKg/videos) 的 Blender 教学视频中感觉到了 Processing 的味道，Processing 很擅长做这样纹理，但是受制于相对单一的表现形式，Blender 丰富的表现形式正好弥补了这一点，可以在此基础上添加更多视觉效果。

# Redjam9 - 几何节点
![image](https://user-images.githubusercontent.com/20842136/123508047-a5847e80-d69f-11eb-8331-14b809f99bc6.png)

[Redjam9](https://www.youtube.com/channel/UCpdGdXzKqCdOjrMR084sMRA/videos) 的视频中大多与几何节点相关，从视频中看的出，他对几何节点了解非常深入，跟着实际案例做练习会收获大量意想不到的收获，期待他接下来的视频。

# Processing - text() 参数
![sketch_117_ParticleMatrix_02_006](https://user-images.githubusercontent.com/20842136/123508741-c2bb4c00-d6a3-11eb-9ad4-a914f558f6cd.png)

![image](https://user-images.githubusercontent.com/20842136/123508143-26437a80-d6a0-11eb-8fe8-4fa89319d12a.png)

最近的工作发现 text 还有这么多可用的参数 [Processing-text()](https://processing.org/reference/text_.html)，x2, y2 可以调节文本框宽/高。

# TEXTUREHAVEN 网站更新
![image](https://user-images.githubusercontent.com/20842136/123508880-9e13a400-d6a4-11eb-82d3-5994cba81905.png)

做三维的朋友应该很熟悉 [TEXTUREHAVEN](https://texturehaven.com/)，他们提供 [CC0 许可](https://hdrihaven.com/p/license.php) 的贴图、HDRI 和三维模型，模型部分相对弱一点，贴图和 HDRI 质量非常好。

![image](https://user-images.githubusercontent.com/20842136/123509095-2ba3c380-d6a6-11eb-8df5-885a17552a35.png)

最近他们做了一点变化，名字改成 Poly Haven，域名 (https://polyhaven.com/) 也跟着变了。但优秀的内容没变，依然强劲，希望他们做的越来越好。

# 莫比乌斯带

![94_PhotoWall_Mobius_01](https://user-images.githubusercontent.com/20842136/123516356-3f632000-d6ce-11eb-9c1a-679ab01d063e.png)

莫比乌斯带是一种只有一个面（表面）和一条边界的曲面，也是一种重要的拓扑学结构。也就是说这种结构没有“正反面”，如果沿着莫比乌斯带行走，永远不会停下来，会无限循环下去。

原理上，一条纸带旋转 180 度，再把两端粘合，就形成了莫比乌斯带。我试着模拟了一下这个结构，用两个弯曲变形器，第一个弯曲 180 度，第二个弯曲 360 度（粘合两端）。

![Snipaste_2021-06-26_22-48-24](https://user-images.githubusercontent.com/20842136/123516855-db8e2680-d6d0-11eb-81e2-e4bf43b7c34a.png)

最终结果看起来没问题，但法线并没有形成莫比乌斯带的结构，这就意味着贴图也不能形成正确的结构。

![Snipaste_2021-06-26_22-49-10](https://user-images.githubusercontent.com/20842136/123516856-dc26bd00-d6d0-11eb-8693-966cc5f491ae.png)

[Default Cube 的教程](https://www.youtube.com/watch?v=deIyUny6s2A&list=LL&index=1) 帮我解决了这个问题，弯曲思路不变，在弯曲后，通过一些技巧修复法线，让法线也能形成莫比乌斯带，这样才保证能后期贴图不出问题，整体形成真正的莫比乌斯带。

![94_PhotoWall_Mobius_02](https://user-images.githubusercontent.com/20842136/123516354-3d00c600-d6ce-11eb-83fd-587d3492db5e.png)

# 工作好朋友

![Cover_01](https://user-images.githubusercontent.com/20842136/123509242-d4eab980-d6a6-11eb-987b-2ce077ba19d3.png)

“工作好朋友”是我在微博上，用来记录工作中发现的工具、方法的标签，最近发现有些东西一条微博说不清楚，可能需要长文章或视频这样图文/演示的方式才能讲清楚。

![image](https://user-images.githubusercontent.com/20842136/123509653-4b88b680-d6a9-11eb-86a8-a35914dc0dce.png)

比如《很大声周刊》的第六、七期封面视频，有感兴趣的朋友问是怎么实现的。其实挺简单的，而且这个效果拓展性很强，稍作改动就可以做出很多种不同的样式，很适合作为经验分享。这个时候一条微博就有点不太够用，本来打算这周把这件事情解决一下，但因为假装很忙就没能实现，下周吧，下周一定。