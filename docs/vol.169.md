# 很大声周刊-vol.169

# Robert Henke - A matter of language 语言的问题
[A matter of language - Science and Research in Digital Arts [2016]
](https://roberthenke.com/interviews/science.html)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/A%20matter%20of%20language.jpg)

> 在数字艺术、媒体艺术和创意编程领域，我们经常会看到一个词：research。
>
> 艺术家会把自己的项目称为 artistic research，展览文案也常常把作品和科学、实验、研究联系在一起。Robert Henke 在这篇文章里直接指出：这件事需要谨慎。
>
> 他的核心观点不是反对艺术家使用科学、工程或技术。恰恰相反，数字艺术当然离不开数学、声音、图像、算法、软件和硬件工程。问题在于，这些研究大多发生在工具层面，而不等于艺术创作本身就是科学研究。
> ...

# 迈向虚幻引擎 6
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/unreal-engine-x-uefn.webp)

> [虚幻引擎 6](https://www.unrealengine.com/news/the-road-to-ue-6?lang=zh-CN) 将推出一个全新的 Gameplay 框架，统称为场景图。该框架是在 Verse 的基础上从零构建的。
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

# Blender 官方界面图标
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/blender-icon.png)

[Blender 官方界面图标](https://ui.blender.org/icons)，结合上一部分，以前使用的机会并不多，但是当前可以根据自己的需求来制作脚本和插件，官方 icon 就很方便，它们本身就完全贴合 Blender 的语境，可以最大限度避免图标和功能语义之间产生偏差。

# Ableton 设计师 Eric Carl 作品页面
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/ableton-hero_2480.jpg)

Ableton 设计师 [Eric Carl](https://ericcarl.link/ableton/) 的作品页面。介绍他在 Ableton 参与的音乐工具界面设计，包括 Live 中的 Auto Shift、Meld、Drift，以及 Ableton Live Design System。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/abl-meld-live.png)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/abl-meld-icons.png)


# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/IMG_2180.jpeg)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/IMG_2220.jpeg)

# It's Conditional - Black Marble
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.169/It%27s%20Conditional-Black%20Marble.jpg)