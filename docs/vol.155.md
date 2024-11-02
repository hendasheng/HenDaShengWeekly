# 很大声周刊-vol.155

# Max 9 发布 / 聊两句节点式操作
![image](https://github.com/user-attachments/assets/6b742055-eece-4097-986c-f9b0aef8b817)

[Max 9 发布](https://cycling74.com/products/max-9)

![image](https://github.com/user-attachments/assets/595b1d54-450f-4def-ab0d-7b17d8e8bd18)

多数没看懂，好消息是加强了对 js 的支持。之前也有，但没用明白，后面会探索一下新版本的代码接口，顺便聊两句为什么代码接口在节点式操作中很重要。

---

节点式交互是兼具易用性和处理复杂工作流程的交互形式，每个节点都可以视为一个特定功能的封装，不同组合形式可以解决不同的问题，甚至可以自定义功能，解决在工作流程中的特定问题。

![image](https://github.com/user-attachments/assets/d0be0309-3fc1-40f5-8f3a-6e11c96c302f)

前面说到每个节点都是一个特定功能的封装，但节点永远不会覆盖所有需求，这个时候就该代码来实现更复杂的逻辑和功能，或者遇到很简单但又非常规的问题，节点覆盖不到，通过代码实现也是更高效的办法，总之节点 + 自定义代码这套组合为整个工作流程提供了极大的灵活性。

** 这里补程序化建模的 gif **

同时节点式操作也意味着它是非破坏性工作流程，也就是说你可以在第一百步时调用第二步的数据，所有数据都可以复用、关联，程序化建模就是充分利用这一点，改变一个参数，所有与之关联的数据都会随之变化。

这就是很多工具采用这种方式的原因，Houdini、MaxMsp、UE、Blender 等等，Blender 本来就可以通过 Python 做程序化控制，但它特别重视的几何节点目前还没有代码接口，我猜接下来的版本中一定会增加这项功能。

# SideFX Labs 
![image](https://github.com/user-attachments/assets/8e9e08db-0ff1-4f46-b765-dd6075fad59b)

![image](https://github.com/user-attachments/assets/fb8c465f-0103-410a-af19-e7faf49f4892)

[SideFX Labs](https://sidefxlabs.artstation.com/projects) 是基于 Houdini 的试验性工具。

# 小白兔白又白
![微信图片_20241102180357](https://github.com/user-attachments/assets/e40d43f7-e6a4-45e7-9020-e29f67896493)

# Steal all the Stars - 雷光夏 / KbN
![image](https://github.com/user-attachments/assets/3d7899a3-ba35-4262-bc72-277e17385f41)
