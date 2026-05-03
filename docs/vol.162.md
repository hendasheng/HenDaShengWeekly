# 很大声周刊-vol.162  Vibe Coding × Blender Python

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/Title_WeChat_162_ChatGPT.png)


# Blender 批量导出插件

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/Blender%20Batch%20Asset%20Export_cn.png)

最近遇到批量导出的需求，于是做了[这个 Blender 插件](https://github.com/hendasheng/batch-asset-export-blender-addon)，将当前选中对象批量导出为 OBJ 和 GLB 两种格式。

常规的批量导出 Blender 本身就能完成，这次的需求有些复杂，希望同时导出 obj 和 glb 两种格式，并且得支持网格、集合、几何节点等等不同属性的对象，这些对象在 Blender 内部有不同的处理方式，所以需要通过 bpy（Blender Python）脚本实现这个需求，也趁机聊聊 vibe coding。

vibe coding 这件事已经火热很久了，但多数讨论集中在前端领域，生成网页、UI、各类小工具等等，原因在于前端天然适合 AI 介入，它本身就是明确可被描述的内容，“描述 -> 生成 -> 验证” 这个循环可被立刻验证，最重要的还有开箱即用的特性，前端不需要复杂的配置也让 AI 更容易地参与到工作流程中。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/Snipaste_2026-05-04_00-20-49.png)

Blender 同样具备这样的特性，但很少被提及，Blender 的 [bpy（Blender Python）](https://docs.blender.org/api/current/index.html) 已经存在很多年了，它几乎可以控制 Blender 中的所有内容。以前 bpy 很少被提及的原因一定程度在于它的入门门槛，首先要理解 API、数据结构等等前置知识，然后才能开始，这一点就足以劝退大部分用户。

现在不一样了，通过 AI，“描述 -> 生成 -> 验证” 的循环也可以快速在 Blender 中实现，不再需要先完整理解整个 bpy 体系，而是从需求本身出发，这意味着以前很多“不值得折腾脚本”的需求，可以通过 AI 实现了。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/Snipaste_2026-05-03_23-45-14.png)

这个导出插件就是这么做的，做成插件完全是我好奇怎么做插件，核心还是 bpy 脚本。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/2026-05-03%2015-58-46_demo.gif)

它可以将选中项（网格、集合、实例、几何节点、曲线）同时输出为 obj 和 glb 两种格式。

除此之外，我还做了不少渲染、命名等等以前看来“不值得折腾”的脚本，它们不是传统意义上尽可能覆盖更多需求的插件，而是专门用于解决具体工作流程的小工具。

这已经和 MCP 的概念有些接近了，不止是生成结果，而是嵌入在流程中。

对我来说这样的小工具有很强的个人属性，它们解决的是非常具体的问题，完全贴合自己的需求，便于在工作流程中反复调用。

你应该也会遇到很奇妙的需求吧，bpy 值得尝试。

# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/IMG_1504.jpeg?x-oss-process=image/quality,q_80)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/IMG_1525.jpeg?x-oss-process=image/quality,q_80)

# Image - Magdalena Bay
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.162/109951169891120142.jpg)