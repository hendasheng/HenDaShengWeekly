# 很大声周刊-vol.70
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_70](https://user-images.githubusercontent.com/20842136/189535336-1153082d-89f8-4a3d-9e9b-60d837b43abb.png)

# Houdini 删除属性时需要注意的问题
![ezgif com-gif-maker (20)](https://user-images.githubusercontent.com/20842136/189538770-f145f47b-d93a-401e-8d3b-7120027f6806.gif)

缓存粒子前根据需求清理属性，可以大大减轻文件容量，从而减少内存压力，保证运行速度。

<img width="889" alt="Snipaste_2022-09-11_18-47-19" src="https://user-images.githubusercontent.com/20842136/189538692-5b3f5c9f-6e6a-4d88-a5c9-ae06c95d5885.png">

但是清理属性时要注意清理哪些属性，有些属性很直观，比如 age、life，如果接下来要用到就保留，否则清理掉。还有些属性不是很直观，但影响很大，比如 id，今天就遇到了这个问题，在粒子缓存后做「重设时间（retime）」，如果清理缓存时没有保留 id 属性，「重设时间（retime）」后会出现闪烁，保留 id 就可以解决这个问题。

<img width="1276" alt="image" src="https://user-images.githubusercontent.com/20842136/189536034-998e343b-cdc0-4705-8fb9-6f448d5900df.png">

解决思路来自[「新的 RETIME 节点闪烁问题」](https://www.sidefx.com/forum/topic/61272/) 中 rpdacosta 的回答。

# 表达式（编程）中开、关（1、0）的用法
![ezgif com-gif-maker](https://user-images.githubusercontent.com/20842136/189536144-58c9031d-b4c1-49d5-85b2-02beddaa62bb.gif)

<img width="972" alt="Snipaste_2022-09-11_18-07-24" src="https://user-images.githubusercontent.com/20842136/189536153-d8f73ad9-a916-4b26-91f1-8dca5351520d.png">

在各类软件的表达式中要注意 0 和 1 的概念，它们在编程中代表「假、真」，也就是「否、是」，这是所有开关的基本逻辑，表达式中也是如此，你不会看到开关之类的按钮，但不代表没有开关功能，0 和 1 就是与之相对的「按钮」。

- [Blender 驱动器面板](https://docs.blender.org/manual/zh-hans/dev/animation/drivers/drivers_panel.html)

- [Blender 表达式](https://docs.blender.org/manual/zh-hans/dev/animation/drivers/drivers_panel.html#simple-expressions:~:text=%E5%85%B6%E6%89%AD%E6%9B%B2%E8%A7%92%E5%BA%A6%E3%80%82-,%E8%A1%A8%E8%BE%BE%E5%BC%8F,-%EF%83%81)

# Blender 在驱动器中实现条件判断
```python
a if condition else b
```
该语法为 [python 2.5 中添加](https://mail.python.org/pipermail/python-dev/2005-September/056846.html)的语法。

**示例：**
``` python
// 当大于 30 帧时开始被驱动旋转
radians(var) if (frame > 30) else radians(30)
```
*这种方式在单独运动时毫无意义，使用场景更多在用一个控制器控制多个对象的时候。*

![ezgif com-gif-maker (19)](https://user-images.githubusercontent.com/20842136/189538560-e4c4d223-b923-4295-8b09-56f86650c824.gif)

<img width="1234" alt="Snipaste_2022-09-12_00-20-51" src="https://user-images.githubusercontent.com/20842136/189538228-618c0645-d43f-400c-a757-3038a2f95b65.png">

# Blender 发布 3.3 长期支持版
<img width="1395" alt="image" src="https://user-images.githubusercontent.com/20842136/189537710-d8cec7d6-47bc-4b67-aa12-36236fdd3871.png">

[Blender 发布 3.3 长期支持版](https://www.blender.org/)

# 小白兔白又白
![IMG_0615](https://user-images.githubusercontent.com/20842136/189535401-2fa953be-058a-4989-86b2-236739ad6c7d.jpeg)
![IMG_0624](https://user-images.githubusercontent.com/20842136/189535417-33729d12-6fee-46ff-ba5e-ffcd3e37e4bf.jpeg)
![IMG_0631](https://user-images.githubusercontent.com/20842136/189535428-0a3992da-be10-4fbb-aca7-550626228839.jpeg)

# 后互联网时代的乱弹 第29期
<img width="942" alt="image" src="https://user-images.githubusercontent.com/20842136/189535462-1e13d173-5688-4d1b-bd86-7df72808ca31.png">

**[后互联网时代的乱弹 第29期](https://www.bilibili.com/video/BV1hG411V7it?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

- 英国**女王去世**再次引发网络论战
- 中共中央政治局首提“**新型举国体制**”
- 高等教育中的**文理之争**
- 缅怀10年代那个**创新乌托邦**

# A Cycle (feat. Odile) - Men I Trust
![IMG_0641](https://user-images.githubusercontent.com/20842136/189538637-6d487f7d-d986-4114-9ce5-23edaaea2e99.JPG)

