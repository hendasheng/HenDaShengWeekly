# 很大声周刊-vol.112
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

# Houdini Vex 和 Vop
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1e07311d-7f49-4a27-9489-43f8994dd7f8)

[Vop](https://www.sidefx.com/docs/houdini/nodes/vop/index.html) 可以理解成节点版的 [Vex](https://www.sidefx.com/docs/houdini/vex/index.html)，相较而言 Vex 更高效，而 Vop 更直观。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cefef733-050b-40ca-b357-06188cebd9ca)


通过 `@age / @life` 影像粒子大小，粒子会随着出生时间的增加越来越大，下面用 Vop 和 Vex 两种方式完成这个需求，或许可以让你对它们有更直观的了解。

## Vop
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ada79eeb-e8e7-451f-b548-698a9789932b)

## Vex
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/30c9dc41-d6c8-4ee4-a820-645df2c8861d)
```C++
float d = @age / @life;
f@pscale = chramp("d", d) * chf("pscale_mult");
```

# 闪烁一切 - Houdini VEX
![ezgif com-optimize (1)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0354517e-2088-4a9e-aa75-1cf74480160e)

通过 **[rand()](https://www.sidefx.com/docs/houdini/vex/functions/rand.html)** 方法产生随机种子，让一切闪烁起来。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/5338b8db-2a41-479d-a852-f4cda088e707)

## VEX
``` C++
float seed = chf("seed");
if(rand(@elemnum + seed) < 0.3 ) i@group_group_sel = 1;
```

## Group Expression
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0886a5a1-e920-43af-8256-1a4c0cdbda05)

[Group Expression](https://www.sidefx.com/docs/houdini/nodes/sop/groupexpression.html)

# 在 Houdini 中创建矢量力场到 Unreal - Gatis Kurzemnieks
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/383260a9-87e3-4260-8800-654e454b8bb8)

[在 Houdini 中创建矢量力场到 Unreal - Gatis Kurzemnieks](https://www.rendereverything.com/vector-fields-unreal-engine/)

> 为了实现这种效果，我们必须创建一个自定义速度矢量场（体积），以特定方式在 3D 模型表面周围移动粒子 - 将最远的粒子移近表面，然后沿着表面向上运动推动它们。由于该速度场是预先计算的，因此它仅适用于静态网格体。使用自定义速度场（速度体积）进行粒子平流是一种非常流行的 VFX 技术。这是一种非常简单但有效的方法，可以实现视觉上复杂的粒子运动，而无需实际运行复杂的粒子逻辑。它也受到虚幻引擎的支持 - 通过 3D 纹理在其粒子系统中采样矢量场（UE 中的速度场只是包含方向的 3D 纹理）每个 3d 点的向​​量 - 类似于 Houdini 中的体积）。 Niagara 的速度也非常快，因此您可以拥有数百万个粒子。

# Blender 3.6 LTS（长期支持版）
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c9a632b6-68a2-4d30-bc5c-6297b6c0dc91)

[Blender 3.6 LTS（长期支持版）](https://www.blender.org/download/releases/3-6/)

![ezgif com-optimize (1)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/09e39d11-15a3-4890-b712-dd0d8c0a28c0)

这次更新最大的亮点是[几何节点](https://docs.blender.org/manual/zh-hans/dev/modeling/geometry_nodes/index.html)开始对物理模拟有了初步的支持，与 Houdini 的工作流程相似，节点式工作流程最好玩的地方在于一切可逆，并且可以关联变量数据，自由度极高，这也是我最近痴迷 Houdini 的主要原因，现在 Blender 也有啦。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/5015cd9a-e631-4987-a65e-c85c1381466b)

还有对大型场景的支持，经过实测（3.5.1 / 3.6）效果显著提升。

Blender 最可爱了。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d3b2baaf-d905-43f7-b641-5ed028497e13)

3.6 也是 3.x 系列最后一个长期支持版，接下来就要开始 4.x 的新阶段了，看到了对 [USD](https://openusd.org/release/index.html) 支持的分支版本。

# Blender → UE -  .GLTF
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/8fef4c7c-c12c-4bd7-8312-ad629a485cd9)

Blender 输出模型资产通常会使用 Fbx 格式文件，可是这样导入 UE 后很容易丢失贴图，需要在导入后笨笨地手动连接。

在这里 [《如何在不丢失纹理的情况下正确从 Blender 导出到 Unreal》](https://www.youtube.com/watch?v=HIzDW4FlC-U) 看到非常好的方法，使用 [Gltf 格式](https://docs.fileformat.com/zh/3d/gltf/) 文件导入 UE，可以完美避免丢失贴图的问题。

# Nascent 新生 - NFT 戏剧表演
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cd6446f1-c793-4a2a-9c09-69dcec48c641)

[Nascent 新生](https://arsnl.art/nascent)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/39c06c25-002b-47ff-a586-f5eb25dd1024)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/e5960136-f993-42e4-9814-082a588a20e8)

---

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/5748d3a8-d2f2-46bf-a5b2-81fef98d7708)

[Ash Thorp Look Book](https://arsnl.art/pdfs/nascent-look-book.pdf)

# Github Copilot - AI 编程工具
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c13f17e9-7f87-4fac-a02c-4447f16791eb)

[GitHub Copilot](https://github.com/features/copilot) 使用 OpenAI Codex 直接从编辑器实时建议代码和整个功能。

# 小白兔白又白
![微信图片_202306302251462](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/721dbfad-beb2-493d-afe3-fdee86def5db)
![微信图片_202306302251464](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/990f5b61-d882-4bac-99ff-775d0b2520b3)
![微信图片_202306302251463](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c7cb701a-ffae-4b0c-ae40-43fb9aee03ba)
![微信图片_20230630225146](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/44784d7a-8e28-4625-ada7-d93307bbeff4)
![微信图片_202306302251461](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/7a8f6a3c-9d53-48e0-a976-fd3c39b40269)

# Describe - Perfume Genius
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/e5a0c4cd-8ece-4e77-9b66-9089b47aff77)
