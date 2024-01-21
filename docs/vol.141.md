# 很大声周刊-vol.141

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/dc379ed0-aca2-4059-b934-955b0d3c8480)

# 在 React Three Fiber 中的使用 Shader
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/6867ef57-6481-4cfa-8e54-f0cad899fe52)

[在 React Three Fiber 中的使用 Shader](https://blog.maximeheckel.com/posts/the-study-of-shaders-with-react-three-fiber/)

Shader 是一个用 [GLSL](https://www.khronos.org/opengl/wiki/Core_Language_(GLSL)) 编写的程序，运行在 GPU 上。它包括两个主要功能，可以输出 2D 和 3 D内容:

- Vertex Shader（顶点着色器）
- Fragment Shader（片段着色器）

它很复杂、很抽象，作者在 R3F 的基础上演示了 Shader 的基本用法。如果你本身也在用 R3F，这篇文章会很有启发，Shader 可以用尽可能底的开销实现更多效果，在对性能极度敏感的实时渲染中会很有帮助。

# Facetype.js - 将字体文件转换为 typeface.js 字体（json） 
Threejs 需要 json 格式字体，[Facetype.js](https://gero3.github.io/facetype.js/) 是一个将常规字体文件转换为 Typeface.js 格式（Typeface.js 是一个 JavaScript 库，用于在网页上实现字体的局部加载和渲染。它的目标是提供一种在网页上使用自定义字体的简便方法，而无需依赖外部字体文件。）的在线工具。

很重要的一点是它有限制字符集（可以选择转换哪些字符）的功能，这对中文字体来说很重要，既可以正常加载中文，还不会出现冗余字体数据。

# CS自学指南
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/687a5716-f4e1-4c60-a1f6-e204600ab932)

[CS自学指南](https://csdiy.wiki/)

# Redshift Render - 随机噪声图案
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b364285d-feca-4914-8837-3eb0c1665e0d)

坚持一下，不要被 Redshift 文档疯癫的排版劝退，有些东西还真离不开它。

[Random Noise Pattern](https://help.maxon.net/r3d/softimage/en-us/Content/html/Sampling+-+Advanced.html?TocPath=Redshift%20Render%20Options%7CRender%20Settings%20-%20Advanced%7CSampling%20-%20Advanced%7C_____0)

> 启用 Redshift 时，将在每一帧上对采样噪点模式进行随机化， 默认情况下这是启用的。
> 
> 诸如景深、运动模糊、蛮力全局光照、高光反射/折射、环境光遮蔽和区域光照等技术共享相同的噪点模式，因此当这些效果的采样数量不足以覆盖噪点并且噪点可见时，噪点可能会在渲染动画时看起来“卡在”相机上。随机化噪点模式使噪点看起来更像是移动的电视静态或胶片颗粒。在某些情况下，这可能更具有视觉吸引力。

但是。

> 在使用动画时，我们建议在使用去噪功能时禁用随机噪点模式！
> 
> 通常情况下，禁用随机噪点模式可能是不理想的，因为它可能导致噪点模式“卡在”相机上。然而，在使用去噪功能时，禁用随机噪点模式可以显著提高效果，因为它最大程度地增加了噪点模式在相邻动画帧之间保持一致的可能性。这减少了在最终去噪结果上出现闪烁“斑点状”干扰的可能性，这可能会非常分散注意力。


# 小白兔白又白
![微信图片_20240121151930](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/98e2b366-231c-40df-9bc3-05d7f1026842)
![微信图片_20240121151933](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cce500fc-90d1-4589-bb1d-69aeb2f8b332)
![微信图片_202401131929231](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/98d78cca-77a2-4c30-b4ea-d50d3b4e4d0d)

# Sky and Sand - Paul Kalkbrenner
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3bb90442-79a3-4956-9413-f9ddc6ee3726)
