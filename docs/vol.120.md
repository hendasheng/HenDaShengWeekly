# 很大声周刊-vol.120
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_120 1](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b583b3cc-3dfa-483a-8e73-149fcddb7a08)

# Houdini UV - 粒子 / VDB
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/14525fbf-256a-4626-851d-0e81423ef7b4)

[Houdini Tutorial: UV mapped Viscous sim](https://www.youtube.com/watch?v=vkiedIaUF3Q&t=3s)

[VDB](https://www.openvdb.org/) - 用于高效存储和操作三维网格上离散的稀疏体数据。

对于它的概念我理解的不是很清楚，目前的状况就是知道流体、烟雾就是通过这种数据格式实现，流体、烟雾都是配合现实世界的描述，而 3d 世界好玩的地方在于“作假”，你可以用流体做一块动态的石头，也可以通过烟雾塑型，最终呈现出流体的形态，等等各种奇奇怪怪，很好玩。

可是关于 VDB UV 的问题困扰我好久，这让我在作假的时候不能使用纹理，这个视频帮我解决了这个问题，用一种很奇妙的方式。如果你也尝试使用 VDB，那大概了会遇到 UV 的问题，这个视频可以帮到你。

# Houdini 混合相机 - ChopNet
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/a6658c15-d2ff-4e24-b659-02e41a7e7df2)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c7101b9a-4753-4f8a-9f06-3a9deff47e30)

- `cam1/cam2` 设置机位；
- `cam_mix + chopnet` 用于混合 `cam1/cam2`；
- 最终输出在 `cam_mix` 上；

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c92180bb-e454-4daa-9fe6-dfe79539a73d)
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/42419b06-01da-46a3-856a-26834759e37b)
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cd7a8ded-543b-4a39-8d3c-ba50ed6b35f6)

![ezgif com-video-to-gif](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/820ddf4b-2568-4c26-ae5b-0efe63a3ee96)


可以通过叠加 [Constraint Simple Blend](https://www.sidefx.com/docs/houdini/nodes/chop/constraintsimpleblend.html) 节点混合多个相机。

## Houdini Chop 模块默认范围
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3a1c16c3-28c8-441c-a212-0f0c4b8b483e)


默认作用时间是 10 秒以内，在混合相机时发现超过 300 帧（FPS-30）之后就失效了，折腾半天才发现是这里的问题。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/75925e6f-ddd0-4435-b6c6-0621ed063cc3)

可以手动延长截止时间，也可以选择完整动画范围的选项。

# 小白兔白又白
![微信图片_20230827175748](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/878c062c-dbca-4388-a0b6-6f9ff5374d6b)
![微信图片_20230827175749](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/bc830c31-3f22-48ea-86dd-ef06b05fc315)

# Covering - Labrinth
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/fef42db3-c058-486c-8982-f964ed61d2e2)
