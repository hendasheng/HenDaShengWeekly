# 很大声周刊-vol.178
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/vol.178-cover.png)

# Loudroom / 大声练琴 - 我做的个人音乐练习工具
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/Loudroom-%E5%A4%A7%E5%A3%B0%E7%BB%83%E7%90%B4.png)

[Loudroom / 大声练琴](https://hendasheng.github.io/dasheng-instrument/0.1/) 是我最近开始做的一个个人音乐练习工具。项目先从吉他开始，目前已经可以选择 Key 和 Scale、查看音阶音、在指板上定位音符，并直接点击试听，也加入了 CAGED 把位、Note / Degree / Root 显示和 Scale 循环播放。

它不是想做成一个传统的乐理课程网站，而是希望把音阶、和弦、指板、听觉、MIDI 和实际演奏慢慢连接起来，变成一个可以直接操作和练习的环境。目前还是 0.1，先把最基础的一条练习闭环做完整，之后再逐步往和弦、节奏、听力和 MIDI 扩展。

# Houdini Redshift 使用 v 计算变形运动模糊
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/houdini_rs_Mesh%20Deformations%20Blur%20From%20Velocity%20Attribute.png)
`Mesh Deformations Blur From Velocity Attribute` 用于让 Redshift 直接读取 Houdini 几何上的 v 属性计算网格变形运动模糊。通常不开也可能已经有 Motion Blur，因为 Redshift 可以通过前后时间采样自行判断顶点运动；只有在缓存、拓扑变化或复杂变形导致这种采样不可靠时，才更需要使用 velocity attribute。

所以当你所有关于运动模糊的设置都已经完成，但某些变形几何就是没有 Motion Blur 时，可以检查几何是否带有正确的 v 属性，并尝试开启这个选项，让 Redshift 直接使用 velocity 来计算运动模糊。

# DeepSeek Harness - 好用且更新速度极快
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/deepseek-harness.png)

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 带来了全新的体验，官方明确指出：“目前还在开发者预览阶段，正在快速迭代。未来将出现破坏兼容性的变更。”

但它依然非常值得尝试。虽然现在还不够稳定，功能和使用方式也可能随时变化，但这种快速迭代本身就很有意思，也能比较直接地感受到它和其他 Agent 工具在使用体验上的不同。

# Patchstorage - 音乐与视觉编程 Patch 社区
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/patchstorage.png)

[Patchstorage](https://patchstorage.com/) 是一个专门分享音乐与视觉编程 Patch 的社区，涵盖 VCV Rack、Pure Data、Max/MSP、Max for Live、Orca、Bela、Bitwig 等大量软硬件平台。你可以在这里直接下载别人制作的合成器、效果器、音序器和生成音乐系统，也很适合把 Patch 拆开研究，看看别人是怎么组织声音、控制与交互逻辑的。

# Electron - 用 Web 技术开发桌面应用
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/Electron.png)

[Electron](https://electron.nodejs.cn/) 可以使用 JavaScript、HTML 和 CSS 开发 Windows、macOS 和 Linux 桌面应用，它把 Chromium 和 Node.js 打包到应用中，因此原本的 Web 前端技术也可以直接用于桌面软件开发。

如果你已经在使用 React、Vite 这类前端技术，Electron 是一种很直接的桌面应用交付方案：除了网页界面，还可以调用文件系统、创建原生窗口和菜单，并最终打包成 Windows 安装程序、macOS DMG 等形式，而不是把源码直接交给使用者。

# Cosmos - 面向创作者的视觉灵感收藏与搜索平台
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/cosmos.png)
[Cosmos](https://www.cosmos.so/) 是一个面向设计师和创作者的视觉灵感收藏平台，可以用来保存图片、建立自己的参考集合，并通过关键词、颜色和视觉相似性继续搜索相关内容。相比单纯的信息流浏览，它更强调把你长期积累的 reference、collection 和个人审美组织成一个可搜索的灵感库。

Cosmos 还会尽量补充图片对应的作者、来源和背景信息，并提供对 AI 生成内容的识别与隐藏选项。对需要长期积累平面、摄影、建筑、3D 和视觉设计参考的人来说，它更像是一个私人化的视觉资料库，而不只是另一个 [Pinterest](https://www.pinterest.com/)。

# Peek Paper - 每日更新的优秀网站设计精选
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/peek-paper.png)
[Peek Paper](https://peekpaper.com/) 是一个专门收集优秀网站设计的每日编辑刊物，定位就是 “The Web’s Daily Paper”。每一期都会人工挑选一批值得看的网页项目，内容覆盖品牌网站、工作室、产品页、实验性网页和交互设计，并保留桌面端与移动端的页面预览。

它和大型灵感图库不太一样，更像一份每天更新的网页设计报纸：数量不会特别夸张，但筛选更明确，适合快速看看最近网页设计在排版、动效、3D、交互和视觉风格上又出现了什么新东西。网站也提供历史 Issues 和 RSS，适合长期当作网页设计参考源来订阅。

# Recent - 每日更新的设计灵感精选
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/Recent.png)
[Recent](https://recent.design/) 是一个面向设计师和开发者的设计灵感平台，每天筛选和更新优秀的设计、网站与数字产品。内容不只限于网页，还包括 Interface、Branding、Typography、Motion、3D、Editorial、Packaging，以及 OG Images、App Screenshots 和 App Icons 等分类。

它最初在 2023 年用来集中整理 X 上出现的优秀设计，2026 年重新启动后扩展到了 Instagram、独立网站和各类设计工具，同时接替了 Godly 的一部分定位。相比大型灵感图库，它更强调编辑筛选和“质量优先”，很适合日常快速浏览最近出现的新网站、视觉风格和数字产品设计。


# 小白兔白又白
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/IMG_2716.jpeg)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/IMG_2745.jpeg)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/IMG_2829.jpeg)

# #20-Aphex Twin
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.178/shape20-Aphex%20Twin.jpg)