# 很大声周刊-vol.181
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/vol.181-cover.png)

# torso T1 - 欧几里得音序器
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/torso-T1.png)

[torso T1](https://torsoelectronics.com/t1) 是一款以欧几里得节奏为核心的算法音序器。你可以先用步数和触发数量快速生成节奏，再通过旋转、概率、重复、随机和调制等方式，让原本简单的模式不断产生变化。

它同时面向创作和现场演出，重点不是提前把每一个音符都写死，而是建立一套可以持续演化的规则，再通过旋钮直接介入节奏、旋律和结构。

## 对我帮助最大的 T1 学习视频
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/T1-learn.png)

[Learn about the Torso T-1 from a music theorist & songwriter](https://www.youtube.com/watch?v=uxIkOTt4zeU)

从基础乐理的角度出发，讲解 T1 各项功能的实际用法。

# 2026 浏览器音频工具地图
一篇比较完整的 [Web Audio 生态梳理](https://labhub.hopto.org/blog/culture/2026-05-16-web-audio-api-browser-audio-2026-audioworklet-tone-js-howler-wavesurfer-peaks-meyda-faust-csound-web-speech-deep-dive?lang=en&utm_source=chatgpt.com)。从底层的 Web Audio API、AudioWorklet，到 Tone.js、Howler.js、WaveSurfer.js、Meyda，再到 Faust、Csound，基本覆盖了现在浏览器中做声音、音乐、音频分析和 DSP 会遇到的主要工具。

它没有把这些库简单放在一起罗列，而是按照用途区分：做音乐、乐器和音序器可以看 Tone.js，游戏音效偏 Howler.js，波形显示与编辑可以看 WaveSurfer.js，音频特征分析则可以看 Meyda。很适合作为进入 Web Audio 生态时的一张工具地图。


# 波函数坍塌（WFC）
[波函数坍塌（Wave Function Collapse / WFC）](https://zh.wikipedia.org/wiki/%E6%B3%A2%E5%87%BD%E6%95%B0%E5%9D%8D%E7%BC%A9)，是一种基于约束进行生成的算法。

它的思路不是直接随机选择结果，而是先定义每个元素之间允许出现的关系，比如某种模块旁边可以连接什么、不可以连接什么。系统会从一组可能性开始，不断根据这些规则排除不合法的结果，直到每个位置只剩下一个确定答案。

它和 [马尔科夫链](https://zh.wikipedia.org/zh-hans/%E9%A9%AC%E5%B0%94%E5%8F%AF%E5%A4%AB%E9%93%BE) 很容易放在一起理解。**马尔科夫链更关心“当前状态之后，下一步最可能是什么”**，生成过程通常沿着时间或序列一步步向前；**WFC 更关心“这个位置在整体约束下还能是什么”**，每确定一个位置，都会影响周围其它位置的可能性。

# katla - 复印合成器
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/genki-01.png)

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/genki-02.png)

>[Katla](https://genki.is/katla) 是一款复音旋转合成器，其灵感源自冰岛最大的冰下火山——卡特拉火山。我们的目标是打造一款配得上这座火山历史的乐器，一款强大而富有表现力的乐器。
>
>Katla 擅长营造丰富、不断演变的多层次音色，每个音符都以其独特的方式涌动、膨胀和爆发。它的设计体现了随机性和可控性之间的平衡，鼓励实验，并满足探索的欲望。

最特别的一点是设备侧板和旋钮都是用真实的冰岛熔岩制成。

# obs-录像转封装
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/obs-%E5%BD%95%E5%83%8F%E8%BD%AC%E5%B0%81%E8%A3%85.png)

OBS 录屏时，更推荐先录制为 MKV，即使录制过程中出现问题，已经录下来的内容通常也还能保留；如果直接录制 MP4，遇到中断时很容易导致整个文件损坏。

但是 MKV 的兼容性并不好，所以最后还是需要 MP4，基于“好录\好用”的前提，依然选择 MKV 录制，完成后通过 OBS 自带的“录像转封装”实现 MP4 转换，这个过程不会重新编码，速度非常快，也不会损失画质。

![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/obs-%E8%87%AA%E5%8A%A8%E5%BD%95%E5%83%8F%E8%BD%AC%E5%B0%81%E8%A3%85.png)

更省力的做法是在高级选项中开启“自动封装至 mp4 格式”。

# 小白兔白又白
![https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/IMG_2969.jpeg](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/IMG_2969.jpeg)

# Pulsar - Ride
![alt text](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.181/Pulsar%20-%20Ride.jpg)