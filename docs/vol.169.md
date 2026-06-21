# 很大声周刊-vol.169

# 迈向虚幻引擎 6
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/unreal-engine-x-uefn.webp)

> 虚幻引擎 6 将推出一个全新的 Gameplay 框架，统称为场景图。该框架是在 Verse 的基础上从零构建的。
> 
> Verse 是 Epic 未来编程模型的基础。这是一种专为驱动大规模、持久化游戏世界而设计的下一代编程语言。在该环境中，全局状态可以正常运行，事务正确的并发由运行时处理。
> 
> 场景图是一个现代化高级 Gameplay 框架，它将为你提供坚实的基础，助你轻松创建游戏和体验，并在不同游戏之间共享可互操作的组件。

开头这部分没太看明白，重点在后面：

> <strong>在虚幻引擎 6 中，LLM、生成式 AI 模型以及 Claude、Codex 等工具将发挥核心作用。</strong> 它们不仅能帮助你更快地创建内容，也能让你在创作过程中保持所需的控制权。
> 
> 我们的一个工作重点，是通过 MCP 协议公开一系列引擎功能。开发者可以自由组合最先进的模型，并基于开放的虚幻引擎 6 MCP 构建各种定制化集成方案。
> 
> 我们也在改进 Epic 开发者助手（EDA），将其作为一种可选的开箱即用解决方案，默认向所有人开放。


# Blender - 充分利用脚本解决重复操作
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/bpy-clear.png)

Blender 里有很多操作本身并不复杂，但一旦需要在大量物体上重复执行，就会变得很麻烦。比如清空选中物体的材质、批量重命名、整理集合、修改显示属性等。

这类重复操作很适合交给 Python 脚本处理。它不一定要写成完整插件，也不需要复杂界面，只要几行代码，就可以把原本需要手动点击很多次的步骤一次性完成。

在 AI 之前，即便是很简单的脚本，手写起来成本还是很高，因为很多关键字、接口是记不住的，查完关键字、用法等等转一圈回来，这个时间大概率比手动操作更久了。

但是 AI 可以让这件事顺畅很多，不需要熟记 blener python 的每一个用法，根据需求通过 AI 的帮助实现脚本，这在具体工作中会有意想不到的效果，会明显减少重复点击、重复设置和重复整理的时间。

```python
#清空选中物体的材质

import bpy

for obj in bpy.context.selected_objects:
    if hasattr(obj.data, "materials"):
        obj.data.materials.clear()

```

