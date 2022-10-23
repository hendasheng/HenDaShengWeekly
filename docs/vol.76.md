# 很大声周刊-vol.76
很大声周刊，在这里记录日常工作、生活所见，每周一发布。
![Title_76](https://user-images.githubusercontent.com/20842136/197400106-0d0a6929-fe41-459d-94d1-608645838d49.png)

# 是什么让生成艺术变得如此困难？
![image](https://user-images.githubusercontent.com/20842136/197334740-7ecf8491-7eef-4bd5-aa5f-5e4fdd7dd1a0.png)

**[是什么让生成艺术变得如此困难？](https://bendotk.com/writing/what-makes-generative-art-hard)**

> 随着过去几个月 NFT 和数字艺术收藏的爆炸式增长，尤其是通过 ArtBlocks.io，我看到人们对生成艺术的兴趣激增。 突然之间，许多人第一次尝试创作生成艺术，因为生成艺术开始被视为一种艺术形式。 生成艺术的世界很大，很难知道应该关注什么。 本文的目的是列出生成艺术家面临的一些痛点，以及新的生成艺术家如何克服这些痛点。
> 
> 我希望这对尝试手艺的新手最有帮助，但观众/收藏家也可能会发现更好地理解这个过程的价值。

# Houdini 拆分、输出 UV 线框图
![6fd355fba3a23c1a96c5a3dd99e5d28](https://user-images.githubusercontent.com/20842136/197334218-55356bdf-c1cc-4643-9c10-e5826c50985b.jpg)

通过 uvunmrap 和 export_uv_wurefrane 两个节点完成拆分 uv 及输出 uv 线框图。

# Processing 新玩法，只用一个摄像头就能追踪人体，手部关节，识别文字...
![640](https://user-images.githubusercontent.com/20842136/197343059-d0ce6241-dad9-4854-8a91-49a48dcbff14.gif)

[Processing 新玩法，只用一个摄像头就能追踪人体，手部关节，识别文字...](https://mp.weixin.qq.com/s/_M2sLRbmEaUXJEDpMmVZcw)

# Houdini VEX 创建几何
![image](https://user-images.githubusercontent.com/20842136/197343229-f83ae610-78fe-4424-a8db-3b3c94053da2.png)

[Houdini VEX 创建几何](https://www.tokeru.com/cgwiki/index.php?title=JoyOfVex14)

# Houdini 去掉重复面
![ezgif com-gif-maker (2)](https://user-images.githubusercontent.com/20842136/197344429-1843998b-123c-4dd4-ab4e-0023ae1de9cc.gif)

类似这样的模型，在完成充气后，中间鼓起，两边是完全贴合的，看起来就像一面，但实际上有两面，程序特别最怕这种情况，并不是运算量大之类的问题，而是面对这种情况它不知道该怎么算。

![ezgif com-gif-maker (4)](https://user-images.githubusercontent.com/20842136/197344924-78a572ed-75e2-4d22-bceb-820477d2d62c.gif)

所以就会出现破面或者点线面乱飞的结果，尤其是在这基础上增加更多物理模拟时，会出现更匪夷所思的问题，我可看了个够，好在找到了解决的办法。

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/20842136/197344920-2f9fed6e-c9a0-4fc2-876c-b186279ceb85.gif)

通过 **fuse** 和 **clean** 两个节点配合，原理很简单，查找距离过近（可控）的点，然后删掉它们就解决啦。

![image](https://user-images.githubusercontent.com/20842136/197344416-0c4b3383-fe2a-4ad1-b868-56243997b2c4.png)

删除前后差异

说起来个很简单，在 Blender 里面几乎是一键解决，还有很多类似的情况，在 Houdini 里面要做更多操作才可以完成，不过更多操作成本带来的是更强的可控性，可以反复调节整个流程中的每一项，blender 那种好像被称为“破坏性”操作，我认为这里的“破坏性”并非贬义，它确实更高效。只是可控性和高效不可兼得，我猜这事儿可能得按需选择。

# Houdini 适合物理模拟的测试模型
![a238dded550c4cdf169ecf56e5e7a55](https://user-images.githubusercontent.com/20842136/197334237-ce6fab36-e68e-4c37-8376-b625eacb3e56.jpg)

做物理模拟时，这狗子特别好，非常适合当作测试模型。
用基础几何图形的问题在于后期替换正式模型后，可能出现意想不到的问题，因为基础模型太简单了，这狗子的好处在于它足够复杂，并且可以通过 vdb 模块自由调节复杂程度，以保证运行速度，它足以覆盖物理模拟过程中可能遇到的大多数问题，它是好狗。

# 小白兔白又白
![微信图片_202210222012104](https://user-images.githubusercontent.com/20842136/197338431-0b17fc11-196e-4891-a279-343c475e8f78.jpg)
![微信图片_20221022201210](https://user-images.githubusercontent.com/20842136/197338412-5bcaae5d-515c-4560-b32c-fe4bd1cbe71e.jpg)
![微信图片_202210222012101](https://user-images.githubusercontent.com/20842136/197338418-fe51819d-1136-4c30-aa57-b495097875d4.jpg)
![image](https://user-images.githubusercontent.com/20842136/197334861-0d1f091b-bb1c-4dd1-90e2-0d5ad9d59bce.png)
![IMG_0918](https://user-images.githubusercontent.com/20842136/197400197-125cb4f6-96ba-49a6-bedd-80421c602043.jpg)
![微信图片_202210222012102](https://user-images.githubusercontent.com/20842136/197338421-18298240-0fde-4780-b47c-aeea5f257ca3.jpg)
![微信图片_202210222012103](https://user-images.githubusercontent.com/20842136/197338428-0b29cb2b-5e5d-414e-af24-f257ef774e9a.jpg)

# 后互联网时代的乱弹 第35期
<img width="954" alt="image" src="https://user-images.githubusercontent.com/20842136/197400305-d46d5325-fa7e-497d-903f-01cf172d8820.png">

**[后互联网时代的乱弹 第35期](https://www.bilibili.com/video/BV1NR4y1Q72g/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# 阿嫂看了出眼泪 - 还潮 / 苍苍老张
![020c68a0642f16a546c38d0d48c9295](https://user-images.githubusercontent.com/20842136/197338822-fb1e2b23-549e-4f22-b6ca-55349f55a09f.jpg)

