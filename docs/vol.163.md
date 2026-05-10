# 很大声周刊-vol.163

# DeepSeek TUI
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/deepseek-tui.png)

尝试 [DeepSeek TUI](https://github.com/Hmbown/DeepSeek-TUI)，顺便聊两句 CLI——命令行工具。

CLI 并不新鲜，它就是命令行工具。可以简单理解成一种更高效、更直接的控制方式，同时也不可避免地更复杂，这也使得多数人在日常工作中不需要用到它。

但是随着 AI 工具的发展，CLI 的应用范围被极大拓展。它可以让 AI 更深度地介入到本地工作流程中。大家熟知的网页 AI 通常是告诉我们“该怎么做”，而 CLI AI 可以直接下场干活，它可以在授权范围内读取本地项目和文件，在真实环境中根据需求完成任务。

当然，不同工作流程中会有不同的用法和需求。但至少有一点是明确的：只要使用电脑，CLI AI 大概率可以在某些环节提高效率。

还有很重要的一点是，一些熟知的 CLI AI 工具因为种种原因，用起来有点复杂，这也劝退了一部分人。或许 DeepSeek TUI 是个不错的切入点，虽然还是有一些前期工作，但并不复杂，至少可以让人更快速地感受一下 CLI AI 的工作方式。

 **补充说明**

>写文章的此刻更新到 v0.8.25，这个版本的 Windows 端的交互出现很严重的问题，最明显的是鼠标滚轮行为异常：在内容区域滚动时，它并不会滚动当前回复内容，而是变成了切换历史输入记录。也就是说，当回复内容较长时，用户很难正常查看上文。与此同时，内容区域也无法像普通终端文本那样正常选中、复制，这会进一步影响实际使用体验。
>
>Mac 端没有这样的问题.

# 自由派音乐理论 / SoundQuest
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/%E8%87%AA%E7%94%B1%E6%B4%BE%E9%9F%B3%E4%B9%90%E7%90%86%E8%AE%BA.png)

[自由派音乐理论 - 中文版本](https://music-theory.aizcutei.com/) | [自由派音乐理论 - 日文原版](https://soundquest.jp/)

> SoundQuest 追求的是一个音乐理论融入日常的世界。
>
>在这个世界里，对于做音乐的人来说，了解理论是一件理所当然的事。多样的音乐对应着多样的音乐理论，它们并不相互争斗，而是能够共存。人们也不会因为围绕理论产生的敌意而感到受威胁，可以用清澈、坦然的心情去谈论和学习音乐理论。
>
>为了走向这样的未来，SoundQuest 提出了一套尊重自由与多样性的音乐理论体系和学习课程模型，并持续追求这一理想形态。
>
> ——  自由派音乐理论 / SoundQuest


# OKLCH：网页颜色的未来
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/OKLCH.png)

>[OKLCH](https://oklch.net/zh-CN#0.66,0.17,295,100) 是 OKLAB 色彩空间的圆柱形表示，由 Björn Ottosson 于 2020 年设计。它代表 OK 亮度、色度和色相 - 与传统的 RGB 或 HSL 系统相比，提供了更直观的颜色处理方式。
>
>与面向设备的 RGB 或具有感知缺陷的 HSL 不同，OKLCH 建立在人类视觉原理之上。它确保相同的数值变化产生相同的感知变化，使其成为创建和谐配色方案和无障碍设计的理想选择。

OKLCH 在实际场景中更偏向设计系统和前端工程。它不一定会出现在每个设计师的日常配色流程里，但已经进入了成熟工具链。

比如 [Tailwind CSS](https://tailwindcss.com/) 的默认色板使用 [OKLCH，daisyUI](https://daisyui.com/) 的主题系统也已经切到 OKLCH；[shadcn/ui](https://ui.shadcn.com/docs/installation) 在 Tailwind v4 体系下也开始把 HSL 颜色转换为 OKLCH，并在主题变量示例中直接使用 oklch()。也就是说，很多人即使没有主动学习 OKLCH，也已经在通过这些工具间接使用它。

# Tone.js - 基于浏览器的声音/音乐制作框架
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/tone-js.png)

[Tone.js](https://tonejs.github.io/) 是一个用 JavaScript 在浏览器中制作声音和音乐的框架。它基于 Web Audio API，但比直接写原生 Web Audio 更接近音乐创作的思路：你可以创建合成器、触发音符、加载采样、添加效果器，也可以用类似 DAW 的 Transport 来同步节奏和安排循环。

Ableton 的 [Learning Music](https://learningmusic.ableton.com/zh-Hans/index.html) / [Learning Synths](https://learningsynths.ableton.com/zh-Hans/get-started) 展示了浏览器音乐学习工具的成熟形态：不需要安装软件，就能在网页里操作节奏、旋律、和弦或合成器参数。

还有很重要的用途是在交互类作品中，通过 Tone.js 来生成声音，而不是在特定条件下播放采样，生成音色可以带来极高的自由度，比如可以根据反馈实时影响声音的音色、滤波、频率等等参数，使得声音和内容有更紧密的关联。

# Houdini 新发现的节点
以前遇到类似需求都是一大堆操作辗转腾挪实现，原来本身就有封装好的功能节点。


## 查找相交点 - Intersection Analysis
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/Houdini-IntersectionAnalysis.png)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/62_IntersectionAnalysis_Geo1.png)

[Intersection Analysis](https://www.sidefx.com/docs/houdini/nodes/sop/intersectionanalysis.html) 查找并输出相交点.

## 查找中心点 - Extract Centroid
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/Houdini-ExtractCentroid.png)

[Extract Centroid](https://www.sidefx.com/docs/houdini/nodes/sop/extractcentroid.html) 查找中心点。


# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/IMG_1754.jpeg)

# Young and Cruel(年少与残酷) - Nova Heart
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.163/Young%20and%20Cruel(%E5%B9%B4%E5%B0%91%E4%B8%8E%E6%AE%8B%E9%85%B7).jpg)