# StringsAlign.js for p5js
![ezgif com-gif-maker (24)](https://user-images.githubusercontent.com/20842136/213120229-7886b55f-ea22-4bd4-ac30-a1ecdba7ef8d.gif)

用于 [P5.js](http://www.p5js.org/) 的字符串对齐工具。

------

# 问题
关于字符串轴心对齐的问题。

![3516c8789ce6a267f4bbcd3e6989d16bb7b393ca](https://user-images.githubusercontent.com/20842136/213129430-c01feec6-90a9-4b40-a0dc-8f5ea89837a9.gif)

``` js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  let tSize = 40;
  let distance = map(sin(frameCount * 0.04), -1, 1, 0, 80);
  leftAlign("abcd", 100, height/2, distance, tSize);
}

function leftAlign(strings, posX, posY, distance, tSize) {
  noStroke();
  textSize(tSize);
  push();
  translate(posX, posY);
  for (let i = 0; i < strings.length; i++) {
    let x = i * distance;
    text(strings[i], x, 0);
  }
  pop();
}
```

最初实现的是基础排列动画，这样只能以第一个字符为轴心运动。

![b0b544ead05d052e35adbbfc681d9f9c97727967](https://user-images.githubusercontent.com/20842136/213130390-1044084d-1c99-478e-b9cb-c9fd29eefc7a.gif)

```js
function rightAlign(strings, posX, posY, distance, tSize) {
  let stringsArray = strings.split("").reverse();
  noStroke();
  textSize(tSize);
  push();
  translate(posX, posY);
  for (let i = 0; i < strings.length; i++) {
    let x = -i * distance;
    text(stringsArray[i], x, 0);
  }
  pop();
}
```

通过倒序算法可以把轴心移到最后一个字符，可使问题在于一开始就先把字符串倒序排列，没办法和前面的动态兼容。

我想怎样才能控制轴心，自由选择字符串中的某个字符为轴心。

# StringsAlign.js for p5js
[StringsAlign.js for p5js](https://github.com/hendasheng/StringsAlign-P5js) 是基于以上问题开发的小工具，可以自由选择轴心，支持水平/垂直排列。

![20230117-191457](https://user-images.githubusercontent.com/20842136/213133191-1abc9688-d151-46a5-b3ed-f5c63b4e635e.gif)

![20230117-192520](https://user-images.githubusercontent.com/20842136/213133124-2c279f47-c59b-44a3-97c5-3700e86cec17.gif)

现在可以很轻松地引用，在 html 文档引入 p5js 后，插入指向 [StringsAlign.js](https://github.com/hendasheng/StringsAlign-P5js) 的链接即可：
```js
 <script src="https://cdn.jsdelivr.net/gh/hendasheng/StringsAlign-P5js@main/scripts/stringsAlign.js"></script>
```
[文档](https://github.com/hendasheng/StringsAlign-P5js)中有详细说明以及示例，欢迎你在此基础上加入自己的奇思妙想，目前还是初级版本，如果在使用过程中遇到问题，欢迎提问、留言，希望你喜欢。🤗 🎉