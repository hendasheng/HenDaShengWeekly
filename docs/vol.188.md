# 很大声周刊-vol.188

# UE × Houdini -  MCP
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/UE-MCP.png)

UE 5.8 版本最重要的升级是提供了[官方的 MCP 插件](https://dev.epicgames.com/documentation/unreal-engine/unreal-mcp-in-unreal-editor?lang=zh-CN)，不必依赖第三方工具。

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.184/banner.webp)

Houdini 虽然没有官方的 MCP，但目前用下来 [FXHoudini MCP](https://github.com/healkeiser/fxhoudinimcp) 这个工具非常稳定好用。

在 AI 工具普及之前，Houdini 和 UE 就已经有紧密的联动能力了，但是涉及到大量的接口、属性和不同的流程，学习成本很高，当两边都能接入 MCP 后，这个问题就得到极大的改善，大量的技术细节可以通过自然语言实现，所以我做了一些尝试。

### 地形
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/984_HeightFirld_Biome_H1.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/984_HeightFirld_Biome_U1.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/984_HeightFirld_Biome_U2.png)

在 Houdini 中完成地形的形态和相关属性，UE 读取属性并渲染。

### 植物分布
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/Houdini%20Biome.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/Houdini%20Biome-01.png)

[Biome](https://www.sidefx.com/contentlibrary/biome-demo/) 是 Houdini 20.5 开始推出的生物群系统，它通过气候、地形演变和植物竞争规则来驱动环境生成，而不是单纯依赖手动绘制遮罩。

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/Houdini%20Biome-02.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/984_HeightFirld_Biome_U3.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/984_HeightFirld_Biome_U4.png)

我尝试在 Houdini 中设置植物的点位置，这样可以最大限度和地形契合，通过 UE PCG 读取这些点的位置，并实现高质量植物群的渲染。

### 程序化建模
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/Houdini%20Rubiks-01.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/Houdini%20Rubiks-02.png)

除了基本形态还有真实模仿的结构关系，我希望它能真正的转动起来，在 Houdini 中完成了基本模型和结构属性的设置。

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/UE%20Rubiks-01.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/UE%20Rubiks-02.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/UE%20Rubiks-03.gif)

在 UE 中根据已有的模型和属性完成渲染和 OSC 控制。


# Kamome-少女スキップ
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.188/Kamome-%E5%B0%91%E5%A5%B3%E3%82%B9%E3%82%AD%E3%83%83%E3%83%97.jpg)
