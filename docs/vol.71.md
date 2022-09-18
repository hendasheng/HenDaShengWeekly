# 很大声周刊-vol.71
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![261_HenDaShengWeekly_vol-71_Title](https://user-images.githubusercontent.com/20842136/190899755-d9a7e2d1-e0dd-4bc5-938a-fe75aa9048ce.png)

# 为 Houdini(19) 和 Blender 安装 ACES/OCIO
![image](https://user-images.githubusercontent.com/20842136/190890748-11d803a7-11e7-4409-b2cb-e475d9a1da60.png)

[为 Houdini(19) 和 Blender 安装 ACES/OCIO](https://www.youtube.com/watch?v=8zb3XjNBgRE)

通过系统环境变量访问 ACES，视频讲解如何将 ACES 安装为 Houdini 和 Blender 都能识别的系统环境变量。

# ACES(学院色彩编码系统)
![image](https://user-images.githubusercontent.com/20842136/190891068-49135b9e-feb7-4394-8bf2-9a8e778b46a6.png)

[ACES(学院色彩编码系统)](https://acescentral.com/)

ACES 是用于交换数字图像文件、管理颜色工作流程以及创建用于交付和存档的母版的全球标准。

它结合了 SMPTE 标准、最佳实践和复杂的色彩科学，由数百名专业电影制作人和色彩科学家在美国电影艺术与科学学院科学技术委员会的主持下开发。

ACES 可用于任何类型的制作，从功能到电视、广告、AR/VR 等等。

ACES 通过在整个制作、后期制作和存档过程中将您的作品的色彩保真度保持在最高水平，从而标准化和简化了色彩管理。

它简化了 DI 中的相机匹配；改善色彩和工作流程沟通；增加了色彩查看管道的可靠性；简化和“未来证明”输出的创建；并且可以帮助为档案创建一个“知道数量”的主文件。

重要的是，ACES 是免费和开源的，因此数十家公司已将其内置到他们的工具中，并在其标准化框架之上不断创新。

# OpenColorIO
![image](https://user-images.githubusercontent.com/20842136/190891103-41257031-8882-446c-a00f-47cd450ef748.png)

[OpenColorIO (OCIO)](https://opencolorio.org/) 是一个完整的色彩管理解决方案，面向电影制作，重点是视觉效果和计算机动画。OCIO 在所有支持应用程序中提供直接且一致的用户体验，同时允许适合高端生产使用的复杂后端配置选项。OCIO 与 ACES 规范兼容，并且与 LUT 格式无关，支持许多流行格式。

# GitClone - GitHub 缓存加速
![image](https://user-images.githubusercontent.com/20842136/190891324-4dbf59a4-ae54-4671-b73f-0d297b1e1a83.png)

通过 git 下载 GitHub 上面的内容，有的时候速度很慢，尤其是大文件。

![image](https://user-images.githubusercontent.com/20842136/190891429-72ab6175-a158-4c02-89bd-998cb0f216af.png)

我在下载 OCIO 配置文件时就遇到了这个问题，通过 [GitClone](https://www.gitclone.com/) 可以添加镜像文件，获取更快的下载速度。

# Blender 应用几何节点
![824cc601470a9de57d7cb7e3f8310f9](https://user-images.githubusercontent.com/20842136/190891518-b25c244c-dc21-4b8c-8310-641f2359bfb8.jpg)

在节点中添加 **「实现实例」** 节点后，修改器才能被「应用」。

# Houdini - 如何访问 Flip 的每个点
![3da05e4c3f54fad972b0ea2403fbb3a](https://user-images.githubusercontent.com/20842136/190891683-98930a9e-e5f0-418b-b08d-ba064966e9cf.jpg)

Flip 也可以像粒子一样通过 @id 访问每一个点，但是默认情况下 Flip 并没有 @id 属性，需要在 **flipsolover -> Behavior** 开启 **Add ID Attribute** 选项。

![image](https://user-images.githubusercontent.com/20842136/190892151-44e2cf79-79c9-4189-b12a-92cf08093b3a.png)

``` C
@v_color = fit(length(@v), chf('v_min'), chf('v_max'), 0, 1);
float cc = fit01(rand(@id + chf("seed") + 1), 0, 1);
@v_color *= cc;
```
这里在速度影响粒子（Flip 粒子）颜色的基础上，还想加入一定的随机值，就是通过 id 属性完成的。

<img width="1276" alt="image" src="https://user-images.githubusercontent.com/20842136/189536034-998e343b-cdc0-4705-8fb9-6f448d5900df.png">

[「新的 RETIME 节点闪烁问题」](https://www.sidefx.com/forum/topic/61272/) 中 rpdacosta 的回答。

上期提到过这个答案，现在讨论的问题，同样受到他的启发。

# 小白兔白又白
![13A50E07-79D7-4CAD-B41D-C71405A0218A](https://user-images.githubusercontent.com/20842136/190896828-d554d449-a1e0-4c29-b1b5-20e4a5832ba9.jpeg)

![6BB260FB-722F-4CBE-A63D-154774EB6712](https://user-images.githubusercontent.com/20842136/190896872-eeebc941-6a95-4c31-ba2d-39efdcc85b80.jpeg)

![D1ED543D-5C28-40FF-BA77-FBAE768B12DC](https://user-images.githubusercontent.com/20842136/190896862-bdbca4de-9149-48c2-868c-55b39cc1902b.jpeg)

![F5C706E9-04BB-4735-B4AE-CF871C2FA639](https://user-images.githubusercontent.com/20842136/190896902-b02f50d7-3512-4c7e-aa7b-36a6358a472b.jpeg)


# 后互联网时代的乱弹 第30期

**[后互联网时代的乱弹 第30期]()**


# Claire - Anyma/Janus Rasmussen
![FFAACFCC-0226-4111-812C-F27EE08EFAE8](https://user-images.githubusercontent.com/20842136/190898073-ad9b384f-b7e4-4f41-b5d6-3a29dacc3dc5.jpeg)
