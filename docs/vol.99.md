# 很大声周刊-vol.99
很大声周刊，在这里记录日常工作、生活所见，每周一发布。
![Title_99](https://user-images.githubusercontent.com/20842136/229352707-8f4ce2bd-751d-4618-a0f6-73a08e7f166d.png)

# 关于 copytopoints 节点的随机属性 - Houdini
![image](https://user-images.githubusercontent.com/20842136/229279786-e8adf40c-244d-4bc7-8a0d-5efbac8a4717.png)

[关于 copytopoints 节点的随机属性](https://www.sidefx.com/forum/topic/89648/?page=1#post-389162)

[Copy to points](https://www.sidefx.com/docs/houdini/nodes/sop/copytopoints.html) 将对象复制到点时，houdini 内置的变量基本都可以通过 [Attribute Random](https://www.sidefx.com/docs/houdini/nodes/sop/attribrandomize.html) 设置随机值，我想知道怎样把自定义变量随机化。

在以前的版本中可以通过 [Copy Stamp](https://www.sidefx.com/docs/houdini/nodes/sop/copy.html) 节点实现，但现在文档中建议通过 [Copy to points](https://www.sidefx.com/docs/houdini/nodes/sop/copytopoints.html) + [Foreach Loop](https://www.sidefx.com/docs/houdini/vex/functions/foreach.html) 的方式完成。

![image](https://user-images.githubusercontent.com/20842136/229280039-0372422c-98e4-4e74-834d-602a670238f5.png)

有点复杂，我在这里 [Houdini Basics - Copy stamp and for each](https://www.youtube.com/watch?v=F87-7bAQgOU) 找到了答案。

# 通过 class (connectivity) 实现面的随机颜色 - Houdini
![image](https://user-images.githubusercontent.com/20842136/229279490-f5304890-7c0b-4a62-add6-129e609357cf.png)

![image](https://user-images.githubusercontent.com/20842136/229279540-32e878d4-f403-4455-9cdc-8c6d9ee57f9d.png)

想给每一块随机颜色，但是默认的随机是针对每一个 Primitive 的。

![image](https://user-images.githubusercontent.com/20842136/229279601-17ad7c16-4dba-4334-b5de-5fc730a9d773.png)

![image](https://user-images.githubusercontent.com/20842136/229279645-2ec19a8e-9321-4c7e-a147-0cafd949482d.png)

[Connectivity](https://www.sidefx.com/docs/houdini/nodes/sop/connectivity.html) 可以将相连的 primitive 连接，并返回 `class` 参数。

![image](https://user-images.githubusercontent.com/20842136/229279725-f393a9dc-1950-4a63-9fe3-f611b16159d2.png)

在设置颜色时通过 `class` 属性，即可实现「每一块随机」。

# 科技爱好者周刊 248：不要夸大 ChatGPT- 阮一峰

[不要夸大 ChatGPT- 阮一峰](https://mp.weixin.qq.com/s/eQBXl53-CH5KmXmd5D_bhQ)

> 我有一种感觉，ChatGPT 已经神化了，仿佛无所不能。
> 
> 今天就来谈谈这件事，我要说，ChatGPT 确实很神奇，是划时代的技术创新，但是不应该无限夸大。
> 
> ChatGPT 有其局限，很多事情它做不到。有人说[11]，ChatGPT 标志着机器取代人类的“奇点时刻”，这是不对的。
> 
> 他们忽略了最关键的一点：ChatGPT 不是“通用人工智能”，而是一个语言模型。
> ...

# Houdini 泰坦计划 Project Titan
![image](https://user-images.githubusercontent.com/20842136/229280335-218f1371-b776-41f6-8907-77c5a65236ba.png)

[Houdini 泰坦计划 Project Titan](https://www.sidefx.com/titan/)

> Project Titan 是一个内部技术演示，旨在生产测试 Houdini 的程序工作流，同时创建一个利用虚幻引擎 5 中最新技术的 3D 环境。为此演示创建的工具和技术将作为学习材料与社区共享并可下载内容。

# Midjourney 样式和关键字参考
![image](https://user-images.githubusercontent.com/20842136/229280495-14692568-c9d4-4e00-9826-4ccbf9178e1f.png)

[Midjourney 样式和关键字参考](https://github.com/willwulfken/MidJourney-Styles-and-Keywords-Reference)

# Midjourney 官方文档
![image](https://user-images.githubusercontent.com/20842136/229280644-e7adf4b6-a7c3-48f3-9639-21c6363cd43b.png)

[Midjourney 官方文档](https://docs.midjourney.com/docs/command-list)

# ChatGPT 中文指南
![image](https://user-images.githubusercontent.com/20842136/229280593-f86ed348-1a4a-4787-b610-69899ad8df4a.png)

[ChatGPT 中文指南](https://github.com/yzfly/awesome-chatgpt-zh)

# 小白兔白又白
![微信图片_20230401175608](https://user-images.githubusercontent.com/20842136/229279303-0970daa1-3e6b-47a7-b36e-1a6c5107b7d9.jpg)
![微信图片_202304011756082](https://user-images.githubusercontent.com/20842136/229279306-a5dcbdc0-a695-4cbd-aa39-ada67b7dadc4.jpg)
![微信图片_202304011756081](https://user-images.githubusercontent.com/20842136/229279311-63939ee7-1d28-4a23-9383-11250d31b289.jpg)


# Daylight - Joji / Diplo
![image](https://user-images.githubusercontent.com/20842136/229280124-bef54d1d-856e-4a60-a813-b2a039d068c6.png)
