# 很大声周刊-vol.182
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/vol.182-cover.png)

# TryCloudflare：本地项目临时公网访问
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/Quick%20Tunnels.png)

在开发需要调用相机、麦克风等设备权限的网页时，直接通过局域网 IP 访问本地开发服务器，浏览器通常会因为不是安全上下文（HTTPS）而限制这些 API。

[TryCloudflare](https://developers.cloudflare.com/cloudflare-one/networks/connectors/cloudflare-tunnel/do-more-with-tunnels/trycloudflare/) 可以快速给本地项目创建一个临时的 HTTPS 公网地址。安装 cloudflared 后，只需要运行：

cloudflared tunnel --url http://localhost:5173

就能获得一个临时的 *.trycloudflare.com 地址。无需域名、DNS 配置或 Cloudflare 账号，很适合用手机测试相机、音频输入、Web Audio 等需要 HTTPS 环境的功能。

# Everything Windows 端文件搜索工具
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/Everything.Search.Window.png)

[Everything](https://www.voidtools.com/zh-cn/downloads/) 是 Windows 上非常好用的文件搜索工具。相比系统自带搜索，Everything 会快速建立文件和文件夹名称索引，输入关键词后几乎可以即时得到搜索结果。

软件本身非常轻量，除了最基本的文件名搜索，还支持通配符、正则表达式、筛选器等高级搜索方式。如果电脑里文件很多，或者经常需要在多个硬盘和项目目录之间找东西，它基本可以直接替代 Windows 自带的文件搜索。

# vgpu - WebGPU TypeScript 库
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/vgpu.png)

[vgpu](https://vgpu.sh/) 是 Vercel Labs 开源的 WebGPU TypeScript 库，用于编写 Shader、3D 场景、GPU 计算等内容。它支持将 .wgsl Shader 像 TypeScript 模块一样导入，并且同一套代码可以运行在浏览器、无界面的 Node.js 和测试环境中。

比较特别的是，vGPU 从设计上就考虑了 AI Coding Agent。它提供了可以直接通过命令行查询的文档、示例和 Shader 检查工具，让 Agent 不只是帮你写 WGSL，也能够获取对应版本的文档、检查代码，并在没有浏览器界面的环境里运行和测试结果。

# MIDI Database - Aphex Twin MIDI 文件数据库
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/midm-database-Aphex%20Twin%20MIDI%20%E6%96%87%E4%BB%B6%E6%95%B0%E6%8D%AE%E5%BA%93.png)

[MIDI Database](http://www.midm-database.co.uk/AFX.html) 是一个非常古早的 Aphex Twin MIDI 文件数据库，按照专辑和作品整理了大量歌曲的 MIDI，可以直接下载，在自己的工具中研究 Aphex Twin 的旋律、节奏和编排。

# 小白兔白又白
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/IMG_2992.jpeg)

# Cyanure Dance - I Hate Models
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.182/Cyanure%20Dance-I%20Hate%20Models.jpg)