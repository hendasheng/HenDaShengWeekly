# 很大声周刊-vol.143
![Title_143](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/eef16f38-8973-4ad4-8eae-61c3772ffb51)

# Houdini 20 新的云工具
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ecd269ab-7d29-4b15-b907-ca2b99b33209)

[Houdini 20 新的云工具](https://www.sidefx.com/products/whats-new-in-h20/environments/)

# Houdini PROJECT PEGASUS 飞马计划
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/74edd98f-f43b-4326-849f-e817ccb726a5)

> [PROJECT PEGASUS 飞马计划](https://www.sidefx.com/pegasus/) 在接下来的几个月中，本部分将通过讨论和教程进行更新，这些讨论和教程将探索用于 Project Pegasus 的生产技术。这将让您更深入地了解 Houdini 和虚幻引擎 5 如何协同工作。

和 [Project Titan 泰坦计划](https://www.sidefx.com/titan/) 类似，通过内部技术演示让用户跟深入地了解 Houdini 和 UE5 如何协同工作。

# Houdini Vex 引用写法
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d6e0b168-2132-4010-8089-edfdb8db35e0)

印象中引用可以直接通过 `v@x = detail("../add1", "P", 0)` 这种写法引用，可是最近发现这么写不行了，虽然不会报错，但不能正确识别。

在这里找到了答案[「VEX 引用其他节点的属性」](https://www.sidefx.com/forum/topic/68385/?page=1)需要通过 `op:` 引用，`v@x = detail("op:../add1", "P", 0)` 这种写法才能能获取正确的值。

# 如何使用 Javascript 只刷新一次页面？
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/f6933c8d-03db-4b3f-96f2-c51f3d1ecb89)

[如何使用 Javascript 只刷新一次页面？](https://mertgursoy.medium.com/how-to-refresh-a-page-only-once-with-javascript-cdbaf079fc73)

``` js
// https://mertgursoy.medium.com/how-to-refresh-a-page-only-once-with-javascript-cdbaf079fc73
// - Mert Kadir Gursoy
function reloadPage() {
 // The last "domLoading" Time //
 var currentDocumentTimestamp =
 new Date(performance.timing.domLoading).getTime();
 // Current Time //
 var now = Date.now();
 // Ten Seconds //
 var tenSec = 10 * 1000;
 // Plus Ten Seconds //
 var plusTenSec = currentDocumentTimestamp + tenSec;
 if (now > plusTenSec) {
 location.reload();
 } else {}
}
reloadPage();
```
# AudioCraft - 音频生成
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/65e06299-5206-448b-88d5-ce83b7b7b59d)

[AudioCraft](https://github.com/facebookresearch/audiocraft/tree/main) 是一个用于音频生成深度学习研究的 [PyTorch 库](https://pytorch.org/) 。 AudioCraft 包含推理和训练代码，用于生成高质量音频的两种最先进的 AI 生成模型：AudioGen 和 MusicGen。

# FreeSound 改版啦
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/bcecc692-4e87-4c32-8015-d955e85d154c)

> [FreeSound](https://freesound.org/) 的目标是创建一个巨大的协作数据库，其中包含音频片段、样本、录音和各种哔声……并根据知识共享许可发布，允许重复使用。 Freesound 提供了访问这些样本的新的、有趣的方式，允许用户：
> 
> - 使用关键字、“类似声音”的浏览方式等以新方式浏览声音
> - 在同一知识共享许可下，将声音上传到数据库或从数据库下载声音
> - 与其他声音艺术家互动！
> 
> 我们还旨在创建一个开放的声音数据库，该数据库也可用于科学研究并集成到第三方应用程序中。使用 Freesound API，研究人员和开发人员可以访问 Freesound 内容并检索有意义的声音信息，例如元数据、分析文件和声音本身。有关详细信息，请参阅开发人员部分和API 文档。 Freesound API 对于非商业用途是免费的，但也可以授权用于商业应用程序。

# 我从来没有过目标 - JASON FRIED
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/bbb72336-bd64-4aca-b390-5db608a95e25)

[我从来没有过目标 - JASON FRIED](https://signalvnoise.com/svn3/ive-never-had-a-goal/)

# Anjunadeep - 独立音乐厂牌
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/84367afe-8295-4e3c-909e-6315200f5dae)

[Anjunadeep](https://anjunadeep.com/us) 是一家总部位于伦敦的独立唱片公司。 Anjunadeep 由Above & Beyond 和他们的经理 James Grant 于 2005 年创立，最初是作为 Above & Beyond 俱乐部专辑中更深层次、更前卫的唱片的出口。如今，该厂牌已成为舞曲音乐最受尊敬的品牌之一。

# Teenage Engineering 出品的工作桌
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/3687c6e7-fbae-4fb3-a1e4-2dbe427544d4)

[Teenage Engineering 出品的工作桌](https://teenage.engineering/products/field-desk)

# 小白兔白又白
![微信图片_20240131220623](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/48ac92d6-ec0d-49ce-ad4d-2d9fb8e5c165)
![微信图片_20240131220624](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/286318bf-a1a9-470e-a40f-3f8e78d47d0e)
![微信图片_20240131220621](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/28bf3637-3902-4656-95ad-209a6b5f8cf7)

# Deceiver - M83
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/1229dfca-54c5-4f6d-b4c9-f6a83918345e)

