# 很大声周刊-vol.124
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_124 1](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/90959708-9bcb-4454-b791-cf6805200613)

# Blender 曲线转网格 / 几何节点
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/e7e6f865-9c27-4dc3-9109-b350a2972f8d)

曲线 [ABC 文件](https://www.alembic.io/) 导入 Blender，我想通过几何节点把曲线转成网格，因为 Cycles(Blender) 不支持渲染曲线，这样才能渲染可见。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ea50a318-8a0d-4f73-a11a-283c7bd479cd)

当前文件已经是曲线类型，所以直接选择曲线转网格，这时会报错。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/aa40bd35-6ffd-4db7-9315-44728760c450)

说输入端是网格（不支持），这个节点只支持曲线输入，可输入端明明是曲线啊。我不知道几何节点的更深层次的运行逻辑，但目前看，在几何节点中，无论曲线还是网格，在组输入中都会被识别为网格。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/26f64cda-e65e-4f5c-9cf0-cf863ebaa723)

这也是上面需求中报错的原因，解决方法很简单，在此之前把网格转成曲线就好了。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/4a25d715-db30-46ed-8af5-1367773b6fa6)

最简单的办法是通过曲线设置完成这件事，不过这种做法的可控性很差，几何节点可以更可控，延展性也更强。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0dd3872b-c414-4428-8652-0eb324f52dfa)

# 小白兔白又白
![微信图片_20230924163646](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d749cfb9-63f1-4488-bb65-e184ed6c1ece)
![微信图片_20230924163654](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/be5f40c4-c078-46bb-8222-b8dfff33d5f3)
![微信图片_20230924163655](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/59118168-263b-473f-8feb-93d2eb90c87d)
![微信图片_202309241636541](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c87e1e2c-ed49-4241-9c93-a657fbe3164f)

# Space Is Only Noise If You Can See - Nicolas Jaar
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/09c339da-4e04-4331-b5e9-f4ea7f674cb9)
