# 很大声周刊-vol.177

# 欧几里得节奏
[欧几里得节奏（Euclidean Rhythm）](https://en.wikipedia.org/wiki/Euclidean_rhythm) 是一种将一定数量的音符（脉冲）在给定的总时间步数中尽可能均匀、对称地分布开来的数学节奏生成方法。

# DeepSeek Harness 开发者预览版
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/deepseek_harness.png)

[DeepSeek Harness（dsh）](https://github.com/deepseek-ai/deepseek-harness/blob/master/README.zh.md) 是由 DeepSeek AI 开发的开源 agent harness（智能体框架）。

我不具备 Agent 工程方面的知识，所以没办法从工程角度分析它。但从使用角度看，DeepSeek Harness 和目前几家的 Agent 产品有很大不同。介绍页面强调“一切皆插件”，其实也没太看懂，实际使用一下感受会更清晰。

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/dns.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/dns_EuclideanRhythm.png)

这是 dsh V4 Flash 完成的介绍欧几里得节奏页面，是一个真实可运行的欧几里得音序器，有一些定制化的问题和细节需要调整。从提出的需求角度看，已经很好的完成了。

DeepSeek Harness 目前处于开发者预览阶段，并没有安装包，需要通过 npm 运行 `npx @deepseek-ai/dsh web`，这里看着有些复杂，实际上这个是更简单高效的方式，稍微了解一下 npm / Node.js 即可，对使用其他工具也会有很大帮助。

# npm / Node.js
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/node-js.png)
npm 是[ Node.js](https://nodejs.org/en) 生态里最常用的包管理工具，全称是 Node Package Manager。它通常会随着 Node.js 一起安装，主要负责安装、更新和运行 JavaScript / Node.js 相关的软件包。

# Blender 5.2 LTS
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/Blender%205.2%20LTS.png)

Blender 发布 [5.2 长期支持版](https://www.blender.org/download/releases/5-2/)，几何节点终于有倒角了。

# Blender MCP 服务器

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/blender_mcp.png)

以前好像都是第三方工具，这次官方推出了 
[Blender MCP 服务器](https://www.blender.org/lab/mcp-server/)。你可以用任意 Agent 调用，通过 MCP 协助完成各种 Blender 内的操作。

我尝试通过 mcp 做基于几何节点的动态，完成度很好。

# Houdini × RedShift OICO 配置
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/houdini_OCIO.png)
OCIO 是 [OpenColorIO](https://github.com/AcademySoftwareFoundation/OpenColorIO) 的缩写，主要负责 Houdini、Redshift 等软件之间的色彩管理和色彩空间转换。

不同工具对 OCIO 的支持和配置有差异，多数情况下工具会自动处理，我在 Houdini × RedShift 遇到颜色配置问题，这篇文章 [Houdini 中的 Redshift 色彩空间 - 渲染中的颜色看起来不正确 / OCIO 色彩空间不可用警告](https://support.maxon.net/hc/en-us/articles/17148723196060-Redshift-in-Houdini-The-colors-in-your-renders-are-looking-incorrect-OCIO-color-space-not-available-warning) 专门回答并解决了相关问题。

# GNM 头部模型导入 Blender
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/gnm_head_blender.png)

[GNM 头部模型导入 Blender](https://nathandickson365.gumroad.com/l/GNMImporter)

# 小白兔白又白

# The Breeze and I - Laurindo Almeida
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.177/The%20Breeze%20and%20I%20-%20Laurindo%20Almeida.jpg)