# 很大声周刊-vol.68
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![01_Compositing_Title](https://user-images.githubusercontent.com/20842136/187061707-f0685458-129e-46ff-a662-83b4a6119836.png)

# Python + FFmpeg 批量修改图片格式
<img width="786" alt="image" src="https://user-images.githubusercontent.com/20842136/187062408-dc692a0a-741b-416e-b434-34b9fdcdc75b.png">

最近工作中遇到的需求是有多个文件需要转换格式，如果只是单个文件转换，在命令行调用 [FFmpeg](https://ffmpeg.org/) 就可以（`ffmpeg -i input.tif output.jpg`），当面对多个文件时，就需要一个脚本来重复执行转换命令，主要功能是转换目标文件夹中的所有文件，并输出到这个文件夹中。

原理很简单，遍历文件夹中的所有文件，给每个文件执行类似 `ffmpeg -i input.tif output.jpg` 这样的转换命令。只需要安装 [Python](https://www.python.org/) 和 [FFmpeg](https://ffmpeg.org/) 就可以使用这个脚本。

[图片格式转换脚本](https://gist.github.com/N1U/0c093f7315a33ae7b800c20d93946d8e)

这不是一个“软件”，做不到开箱即用，需要了解一些关于 Python、命令行等等基础前置知识，真的很基础，我的编程能力很差，这个脚本也是根据需求边查询相关用法边写的，比如 [Python os 模块](https://docs.python.org/zh-cn/3/library/os.html) 是用来操作文件路径的，转换文件格式前提是先要找到这个文件，[Python subprocess 模块](https://docs.python.org/zh-cn/3/library/subprocess.html) 用来执行相关命令，脚本中 `ffmpeg -i input.tif output.jpg` 这样的转换格式命令就是通过 **subprocess** 来执行的，除此之外就是基本的 Python 语法了，整个过程用了半个多小时，再遇到这样的需求只需要运行一下这个脚本就可以。如果你对编程感兴趣，从这样简单并且能解决实际问题的案例入手可能是不错的选择。

# FSpy - 图片摄像机适配软件
<img width="775" alt="image" src="https://user-images.githubusercontent.com/20842136/187067437-3bd9f193-3ee3-4dd5-936f-1cccb4208be2.png">

[FSpy - 图片摄像机适配软件](https://fspy.io/) 

![image](https://user-images.githubusercontent.com/20842136/187067516-429dd54a-c57c-447f-a63c-a21f91f5bb2f.png)

根据自定义消失点计算摄像机在 3d 环境中的相对位置。最近工作中遇到实景合成的需求，FSpy 专门就是干这个的，但是也发现了一些问题，它需要画面中就很清晰的平行、垂直线，越清晰计算越准确，可是有些情况下画面中并没有清晰的线条，这就很难办，我在想如果拍摄前期在画面中增加一些参考点应该会好一点，就像影像追踪中的小黑点那种，但具体怎么加参考点还没想明白。

# 原声吉他在线调音器 - Fender
<img width="1410" alt="image" src="https://user-images.githubusercontent.com/20842136/187067908-57a3020e-634d-4e0b-b8d1-33e41285ef42.png">

[原声吉他在线调音器 - Fender](https://www.fender.com/online-guitar-tuner/acoustic-guitar-tuning)

# Houdini中物体旋转的原理（矩阵、四元数）
<img width="940" alt="image" src="https://user-images.githubusercontent.com/20842136/187067961-b3200064-08f1-41ec-9ee7-84f7dbdd28fe.png">

[Houdini中物体旋转的原理（矩阵、四元数）](https://www.bilibili.com/video/BV154411k7Ho/?vd_source=6c68891752436b0097051bf700e169a9)

# 小白兔白又白
![IMG_0536](https://user-images.githubusercontent.com/20842136/187067793-38f40c5d-3c2c-4067-837d-f008b317cedc.jpg)

![IMG_0546](https://user-images.githubusercontent.com/20842136/187067785-7c6e5dde-596c-437d-b09d-d9936f836f22.jpg)

![IMG_0553](https://user-images.githubusercontent.com/20842136/187067783-f16dee33-f65a-4ef1-a5b6-f2f3ef387993.jpg)

![IMG_0556](https://user-images.githubusercontent.com/20842136/187067782-2ebd376e-4a97-4588-a27a-b4267447c166.jpg)

![IMG_0538](https://user-images.githubusercontent.com/20842136/187067788-2038f145-d5fb-45ae-b1c7-ba0c6128fd03.jpg)

![IMG_0552](https://user-images.githubusercontent.com/20842136/187067780-8e7fa206-8b08-4972-8903-5655ecd19d67.jpg)

# 后互联网时代的乱弹 第27期
<img width="949" alt="image" src="https://user-images.githubusercontent.com/20842136/187078956-f17f87fe-ba3e-4f91-a14a-1c08791c1b4b.png">

**[后互联网时代的乱弹 第26期](https://www.bilibili.com/video/BV1EN4y1c7w1?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

- 日本文部科学省「中国科研论文无论数量质量均登顶第一」
- 从现行**法的精神**看 AI 创作品的著作权
-  任老板和马老板们的**寒气**你感受到了吗？
- 围绕「**新版红绿灯**」的 24 小时魔幻之旅
- 教育部公示 2022-2025 年中小学竞赛活动
- 我们如何看待中小学的各种竞赛活动


# Time Is Running Out - Why Mona/Unlike Pluto
![IMG_0560](https://user-images.githubusercontent.com/20842136/187071586-9cc5331d-9d92-4619-80fd-8a1d498af102.JPG)

