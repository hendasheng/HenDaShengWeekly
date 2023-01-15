# 很大声周刊-vol.88
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_88 1](https://user-images.githubusercontent.com/20842136/212282709-d3a62c88-d7a3-4012-917f-df75dbb27662.png)

# Houdini 预览视图中开启摄像机景深
<img width="1159" alt="e89e62472646ec95bd0a250e2e5ac79" src="https://user-images.githubusercontent.com/20842136/212258241-f0228d8f-8110-4338-975e-a038428a3ced.png">

# Blender Kit - 网络不灵的时候怎么办
![image](https://user-images.githubusercontent.com/20842136/212259176-767ebc70-0ce6-4dbd-ba1c-013db631b311.png)

<img alt="da5dce1ed96f6ec48d4e571b350111e" src="https://user-images.githubusercontent.com/20842136/212259646-6ab8abef-5b8c-402a-8981-e14ebaa1ae2d.png">

[Blender Kit](https://www.blenderkit.com/) 是提供各类 3D 资产的社区，可以在 Blender 内部直接调用，但是有的时候会出现网络问题，在设置中[调整「IP 版本」和「代理选项」](https://github.com/BlenderKit/blenderkit/issues/443)可以解决这个问题。

# Houdini - Retime 保护 UV
<img  alt="85dbea69631deca8593fece756cd8c3" src="https://user-images.githubusercontent.com/20842136/212259799-4d983f3d-f763-4337-9bb8-2d5682d2955a.png">

对有 uv 信息的模型做 [Retime](https://www.sidefx.com/docs/houdini/nodes/sop/retime.html) 处理时，uv 会出现近乎癫狂的抖动，在属性中注明 `^uv` 即可让 uv 不受影像。

![image](https://user-images.githubusercontent.com/20842136/212260814-e94b267d-45b9-4ed5-9ed2-851a11f4b9c2.png)

「^uv」这种写法在 Houdini 中通用，比如在删除属性时，框选的两条分别指：
- 删除所有属性 `*`
- 同时保留 Cd `^Cd` 和 UV `^uv` 属性

# Houdini VEX 创建组
![256_VEX_SelectGroup](https://user-images.githubusercontent.com/20842136/212261278-08060d8d-5a45-4442-8f5d-521f304ecb94.gif)

```
if(@P.y > chf("group_ramp")) 
    i@group_top = 1;
```
示意代码指的是根据 y 轴 `@P.y` 高度创建组（group_top），接下来就可以有针对性地对分组进行各种操作，比如示意中的填色。

# Group Promote - Houdini 组类型转换
![image](https://user-images.githubusercontent.com/20842136/212264525-eaa81714-2c71-4393-a5d7-1b422e85055a.png)

奇怪测试。我想对选中的组做置换，原本的面数不够，所以要给选中的组做 `remesh` 处理，获得更细腻的置换效果，可是 `remesh` 只作用于面，刚刚选中的是点，所以需要对组做类型转换。

![image](https://user-images.githubusercontent.com/20842136/212266910-32de3fb7-f0af-4637-8f5e-33373f2b15c2.png)
[Group Promote](https://www.sidefx.com/docs/houdini/nodes/sop/grouppromote.html) 就是干这个的，

![ezgif com-gif-maker (4)](https://user-images.githubusercontent.com/20842136/212267784-70518295-43f5-495e-bcb0-734f2fb6858d.gif)

转化数据类型后就可以对选中组做 `remesh` 处理，获得更细腻的置换效果。

---

![image](https://user-images.githubusercontent.com/20842136/212266987-d17f92f7-ded7-473a-acdb-eb822f007ffa.png)

当然，还可以在选择分组时，直接选择 `Primitives` 类型，就不用转来转去了，不过在奇怪测试中，怎么莫名其妙都不奇怪。

而且在实际工作流程中确实有在不同阶段需要不同的数据类型的情况。

# Houdini 中的「点线面」
![image](https://user-images.githubusercontent.com/20842136/212268464-ea8a7f06-8d4d-45fd-bea9-f0dd349af30b.png)

Houdini 中关于「点线面」的概念和常规的认知不太一样，这里讲的很清楚 [Points and Verts 和 Prims](https://www.tokeru.com/cgwiki/index.php?title=Points_and_Verts_and_Prims)。

# Houdini Peak，点、线、面沿法线平移
![ezgif com-gif-maker (5)](https://user-images.githubusercontent.com/20842136/212270080-5f11d42a-e958-4052-8995-f577ef5924e5.gif)

[Houdini Peak，点、线、面沿法线平移](https://www.sidefx.com/docs/houdini/nodes/sop/peak.html)

# Three.js零基础入门教程(郭隆邦)
![image](https://user-images.githubusercontent.com/20842136/212280702-d1acd524-3dd9-44eb-b0f5-182ea1aad86f.png)

[Three.js零基础入门教程(郭隆邦)](http://www.yanhuangxueyuan.com/Three.js/)

# 小白兔白又白
![微信图片_20230113210936](https://user-images.githubusercontent.com/20842136/212327454-fcc48f9c-ebaf-45c6-bdb2-e423e284c525.jpg)
![微信图片_202301132107304](https://user-images.githubusercontent.com/20842136/212327122-10eb3ec3-5607-414a-b48a-666cb05822ae.jpg)
![微信图片_20230113210730](https://user-images.githubusercontent.com/20842136/212327105-23680306-40ff-4ffb-ae96-6a894ae74ed6.jpg)
![微信图片_202301132107303](https://user-images.githubusercontent.com/20842136/212327120-604de661-b06e-453c-839f-38443a249569.jpg)
![微信图片_202301132107302](https://user-images.githubusercontent.com/20842136/212327116-4701e51e-8e24-446a-b23d-bee104e566be.jpg)


# 后互联网时代的乱弹 第47期
<img width="901" alt="image" src="https://user-images.githubusercontent.com/20842136/212538163-9408ab36-809a-4af0-8c61-624c7a3028d6.png">

**[后互联网时代的乱弹 第47期](https://www.bilibili.com/video/BV1YM411b7wj/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# Edge of a Dream - The fin
![image](https://user-images.githubusercontent.com/20842136/212328172-68442610-a122-4305-b4b7-b1faa99ca198.png)