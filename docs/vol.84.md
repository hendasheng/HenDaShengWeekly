# 很大声周刊-vol.84
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_84](https://user-images.githubusercontent.com/20842136/208156363-2bb280e9-a00e-44fb-b796-2804577b9601.png)

# 关于 Houdini Vex 数据类型

Houdini VEX 对于是否写明数据类型不那么敏感，多数情况不写也没关系，我就是这么干的，这不就遇到问题了么。

![image](https://user-images.githubusercontent.com/20842136/208157290-5bde39d2-4d44-4897-869c-4e8fa473d158.png)

想让速度值等于法向 `@v = @N`，可结果是错误答案，折腾好半天才想到数据类型的事儿，两个值都是向量类型（Vector），试着写成 `v@v = v@N` ，果然得到了预期结果。

![image](https://user-images.githubusercontent.com/20842136/208157398-cba3db53-ab85-4d62-817c-4cfc7462caaa.png)

问题确实出在没写明数据类型上，在可写可不写的情况下，写了准没错。

# Houdini 沿法向旋转
![5cd04c1ecf32fe57b262655c4ae2101](https://user-images.githubusercontent.com/20842136/208162393-2b95780a-3c93-4372-a61d-f14bb02aef49.png)

# IES Library - 使用真实世界的照明进行更好的渲染
![image](https://user-images.githubusercontent.com/20842136/208156794-4f480e6c-4c54-48ac-b860-3e8151974645.png)

[IES Library](https://ieslibrary.com/en/home?continueFlag=69722874560b322db02ce80e50779af6)
> IES 文件描述了灯发出的光如何在房间内分布。该数据由许多制造商提供，因此照明设计师可以逼真地模拟使用特定光源时项目的外观。
>
>3D 艺术家也使用这些数据来更逼真地计算他们的图像。但是，使用试错法找到正确的文件很麻烦，因为制造商不一定包含可视示例。
>
>为此，创建了此页面。我们用制造商数据丰富了现有的 IES 集合，最终达到了近 200,000 条数据。我们使用 Python 读取数据，将内容散列为 MD5，并将数据分配给各个制造商。因此我们消除了重复项。在这个过程之后，“只”剩下 160,000 条数据。
>
>之后，我们在 Blender 中创建了一个场景，其中光源悬挂在墙前 5 厘米处和地板上方 1 米处。然后我们使用 python 为每个 IES 文件自动计算这个场景。
>
>目标是预览图像应该具有大致相同的亮度。因此，我们首先必须计算预览并测量最大亮度，调整光强度，最后计算图像。在此过程中，过滤掉太暗的数据（发光强度=无穷大）

# 载入3D模型（Loading 3D models）- three.js
![image](https://user-images.githubusercontent.com/20842136/208159911-68c1e6db-0445-41da-9852-0c5c66f2de9b.png)

[载入3D模型（Loading 3D models）- three.js](https://threejs.org/docs/#manual/zh/introduction/Loading-3D-models)
目前 Web 端有关 3D 的内容多数都基于 [three.js](https://threejs.org/)，这是一份关于文件格式的指导。

# CHARGE - Blender Studio 的第 14 部公开电影
![image](https://user-images.githubusercontent.com/20842136/208234594-b230c499-0e0c-479c-9c2d-89eb66881f2e.png)

[Charge - Blender Open Movie](https://www.youtube.com/watch?v=UXqq0ZvbOnk)

> Blender Studio 的第 14 部公开电影是一部视觉冲击力强、动感十足的 2 分钟动画，其灵感来自于游戏电影和实时演示格式。
>
>该项目的目标是挑战 Blender 和创意团队追求真实感，并推动 Blender 在交互式 PBR 工作流程中的能力。
>
> [Blender Studio - Charge](https://studio.blender.org/films/charge/)

## 更多 Blender Studio 出品的电影
![image](https://user-images.githubusercontent.com/20842136/208234777-adada02d-8253-4b7d-ae57-e31cfbbd97dc.png)

[Blender Studio - Films](https://studio.blender.org/films/)

# 安田昂弘 - 平面设计师
![image](https://user-images.githubusercontent.com/20842136/208157516-57246e2f-5abf-4686-b897-4c7048c6bc29.png)

平面设计师安田昂弘的[作品页面](![image](https://user-images.githubusercontent.com/20842136/208157516-57246e2f-5abf-4686-b897-4c7048c6bc29.png)
)，交互体验优秀，他也是创意团体 [CEKAI](https://cekai.jp/) 成员。

# Ping.eu - 线上 Ping
![image](https://user-images.githubusercontent.com/20842136/208157779-c8b2823a-6cc8-4e82-a83d-be32eb3de572.png)

[Ping.eu](https://ping.eu/?continueFlag=69722874560b322db02ce80e50779af6) - 线上 Ping。

![image](https://user-images.githubusercontent.com/20842136/208158145-a6634d82-57a7-4cae-ab88-b9bf4e3b8a1e.png)

[ping 命令](https://www.ibm.com/docs/zh/power9/9080-M9S?topic=commands-ping-command)

# 在网页中置入响应式 P5.js 画板
![image](https://user-images.githubusercontent.com/20842136/133890585-81d90438-481e-40cb-98e5-c89cee303124.png)

[在网页中置入响应式 P5.js 画板](https://mp.weixin.qq.com/s?__biz=MzAxOTM5MzY1Ng==&mid=2648610553&idx=1&sn=a6928da6ca2abcca2402d0dbb1bb0593&chksm=83ed8beeb49a02f8e99728a02a9afc39672843f488ca54384e2c8c853c1cb302483394967c66&token=1025703500&lang=zh_CN#rd)

最近遇到类似需求，已经彻底忘干净了，看了看以前写过的文章，还能用得上。

# USD - 通用场景描述
![image](https://graphics.pixar.com/usd/images/piper-banner.jpg)
[USD](https://graphics.pixar.com/usd/release/index.html) 是一个高性能的可扩展软件平台，用于协同构建动画 3D 场景，旨在满足大型电影和视觉效果制作的需求，由[皮克斯开发并开源发布](https://graphics.pixar.com/usd/release/press_opensource_announce.html)。

## USDZ - 向 Apple 设备提供 AR 和 3D 内容
![image](https://user-images.githubusercontent.com/20842136/208164243-914efc84-c666-4f0e-a871-c82916ca501b.png)

[USDZ - 向 Apple 设备提供 AR 和 3D 内容](https://developer.apple.com/documentation/arkit/usdz_schemas_for_ar)

Apple 与 Pixar 合作开发了一套新模式，以进一步扩展 AR 用例的格式。

## Reality Converter - 将 3D 文件转换为 USDZ
![image](https://user-images.githubusercontent.com/20842136/208159358-6c3d286e-62c2-4057-a049-2eec277f0d61.png)

[Reality Converter - AR Kit 文件格式（USDZ）转换工具](https://developer.apple.com/cn/augmented-reality/tools/)

# 后互联网时代的乱弹 第43期
![image](https://user-images.githubusercontent.com/20842136/208313210-d1af556b-e018-4124-a429-949c89fd869f.png)

**[后互联网时代的乱弹 第43期](https://www.bilibili.com/video/BV1TD4y1h7uh/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# Tactics - Japanese Breakfast
![image](https://user-images.githubusercontent.com/20842136/208159007-4a6eaf11-399a-4859-bf7f-2cf14b605265.png)
