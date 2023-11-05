# 很大声周刊-vol.130
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b4abf9d7-5fa2-4a4a-b4f6-0ee2864c6bcc)

# bbox 用法以及为啥要搞这么复杂 - Houdini
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/24782f4f-6631-47c6-926b-3bd73db74ad4)
[bbox](https://www.sidefx.com/docs/houdini/expressions/bbox.html)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b7df7301-74d1-4ea3-af9d-6b3857d1d8e6)
`bbox("../box1", D_XSIZE)/2 + bbox("../sphere1", D_XSIZE)/2`

`bbox(surface_node, type)` 用来获取对象的边界范围。直接写参数是最简单直接的方式，但是在面对复杂程序化建模时，需要通过这种获取变量的方式关联各个物体的关系。

![ezgif com-video-to-gif (7)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/7a8e3f54-332f-42ad-8622-7a92af5725dc)

# JS 干掉数组中的多余元素 / 保证运行性能
![Alt text](<ezgif.com-video-to-gif (8).gif>)

示例中是一大堆慢慢下落的粒子，鼠标点击画面时在随机位置增加粒子，粒子掉出画面只是在视觉上消失了，但是在存放粒子的数组中仍然存在，这就意味着随着运行时间增加，粒子数量也在不断增加，增加到一定数量时浏览器就该崩溃了。

对于性能的要求，实时运行的应用（P5js\Touchdesigner\...) 要比预渲染应用 (Blender\Houdini) 敏感的多，示例中所指的情况，理想状态应该是粒子调出画面时，数组中的数量也要减掉这部分，然数组长度维持在一定长度。

所以需要为粒子设置条件判断，判断它是否在画面中。

``` js
this.finished = () => {
    if (y > height) return true;
  };
```

在循环中检测，如果它掉出画面外，就从数组中删除。
``` js
for (let i = 0; i < bubbles.length; i++) {
    let b = bubbles[i];
    b.update();
    b.display(); 
    // 检测并删除
    if(b.finished()) bubbles.splice(i, 1);
  }
```

![Alt text](<ezgif.com-video-to-gif (9).gif>)

这样就保证了数组长度和视觉看到的一样，无论怎么运行也不会把浏览器搞崩溃。

有些时候直接在循环中删除可能会引起数组长度报错，还可以通过反向循环的方式，删除指定元素。

```js
 for (let i = 0; i < bubbles.length; i++) {
    let b = bubbles[i];
    b.update();
    b.display();

    // if(b.finished()) bubbles.splice(i, 1);
  }

  for (let i = bubbles.length - 1; i >= 0; i--) {
    if (bubbles[i].finished()) bubbles.splice(i, 1);
  }
```

**示例代码**

```js
let bubbles = [];
function setup() {
  createCanvas(800, 600);
  for (let i = 0; i < 100; i++) {
    bubbles[i] = new Bubble(random(width), random(height), random(5, 20));
  }
}

function draw() {
  background(220);

  for (let i = 0; i < bubbles.length; i++) {
    let b = bubbles[i];
    b.update();
    b.display();
    // if(b.finished()) bubbles.splice(i, 1);
  }

  for (let i = bubbles.length - 1; i >= 0; i--) {
    if (bubbles[i].finished()) bubbles.splice(i, 1);
  }
}

function mousePressed() {
  bubbles.push(new Bubble(random(width), random(height), random(5, 20)));
  console.log("Bubbles Length: " + bubbles.length);
}

function Bubble(x, y, r) {
  this.x = x;
  this.y = y;
  this.r = r;

  this.update = function () {
    y += 2;
  };

  this.display = function () {
    fill(0);
    circle(x, y, r);
  };

  this.finished = () => {
    if (y > height) return true;
  };
}

```

# 小白兔白又白
![微信图片_20231105163541](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/77c5e4ad-6da0-4013-b94c-32cabc9a9886)
![微信图片_20231105163540](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/163d4607-0115-4c04-b45f-9f239ff17f8a)
![微信图片_20231105163539](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/29d0caa1-ad92-4fe7-bfef-813cae9a1873)

# La La La - Midnight Generation
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/5494b985-b09b-4a69-8632-a074b761c918)
