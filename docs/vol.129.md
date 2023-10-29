# 很大声周刊-vol.129
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_129](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/fa83a4bc-73bb-47fd-b09f-32fe187a6e8b)

# Houdini 在 Font Node 中获取属性字符串信息
![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/5186ecdd-94a6-4f2a-9949-66ea6228c29b)

我知道如何通过 [HScript](https://www.sidefx.com/docs/houdini/commands/index.html) 获取一个属性信息。

![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/eb010955-eff2-426a-aa2f-b27c1e7d33b8)

先通过 vex 将属性转换为 Detail 信息，在 Font Node 中通过 `detail("../get_point_pos", "y_pos", 0)` 获取值。

可是需要多个属性值的时候就搞不定了，刚开始觉得可以通过常规的循环完成。

![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/38d099b4-03e0-48e7-a326-0aee2db929e0)

可是 Font Node 没有输入接口，也就没办法放在循环中。试了很多办法，都不能完成需求，最后在论坛中提问 [“如何获取点位置字符串？”](https://www.sidefx.com/forum/topic/92658/) 得到了答案。

![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/c218e937-cd88-4df1-acf3-4e294f8f1062)

彻底解决了我的问题，是一种完全没见过的方法，大概是通过自定义接口，将参数传进来，这种传法会有一些限制，应该算是非常需求时的非常手段？我现在也很难解释清楚。houdini 的节点都支持不同类型的自定义参数，利用好这一点可能会让很多事情变得更简单一些。

# Blender 几何节点 - 挤出网格没有底咋办？

![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/682edfd3-5f7b-49aa-85c6-c71690814ea0)

目前的节点中并没有自动填充底面的选线，不过可以用最质朴的方式找补回来。

![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/f2d2fd01-0b82-4ca2-8058-561b20e8ecc4)

# 对比 Processing / P5js 和 Touchdesigner 中画曲线的方式
![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/0809ab24-6f3c-4c09-aeaa-134713792476)


## P5js / Processing
``` js
let total = 90;
let radius = 200;
let freq = 10;
let offset;

function setup() {
  createCanvas(800, 600);
  noFill();
  stroke(0);
}

function draw() {
  background(220);
  
  offset = -frameCount * .08;
  let inc = map(noise(1), 0, 1, 1, 10);
  
  beginShape();
  for (let i = 0; i < total; i++) {
    let x = sin(i * radians(freq) + offset) * i * 5 + width/2 - radius/4;
    let y = i * 10 - 10;
    curveVertex(x, y);
  }
  endShape();
}
```

## Touchdesigner
![image](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/a04457fc-99ab-44e3-ac1e-393b20008137)

同样是 sin 函数，在不同平台中，根据平台特性有着不同的实现方式，但原理完全相同。

# Houdini 20 Keynote
![345d1571a5444f88b3f1895b8bbdf97](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/32f88f24-4c29-4b62-b6d1-cbd197ef0857)

[Houdini 20 Keynote](https://www.sidefx.com/community/houdini-20-keynote/)

> 10 月 25 日在英国伦敦 Curzon 电影院现场录制。您已经看过先睹为快，现在您终于可以了解有关今年 11 月 Houdini 20 即将推出的所有最新功能的更多信息。

# 小白兔白又白
![微信图片_20231029230417](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/6918bfdb-307d-4e38-9032-e915c74ce7f3)
![微信图片_20231029230419](https://github.com/hendasheng/lirujinzhi-web/assets/20842136/5a08f2eb-087d-41e3-ac75-209f0a42b161)

# Some Kind of Game - A.A.L
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/cc3f9fbe-122f-40e1-a31b-2c2c32dc401b)
