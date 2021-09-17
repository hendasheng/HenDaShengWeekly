我想把 P5js 当作一个元素插入到网页中，而不是像往常那样页面中只有 P5js 画板，想着应该挺简单的。

P5js 原理上是在 HTML 结构中插入一个 canvas 标签，只要调整尺寸和插入位置就好，实现上面的需求并不难：
1. 首先在 html 中添加一个空标签，给它一个 id（class 也可以，从语意上讲 id 更合适，「id」偏向唯一，「class」偏向集合），这个 id 的作用像是锚点，js 通过它来定位画板在页面中的位置。
    `<div id="p5Element"></div>`

2. 在 js 文件中创建画板，找到刚刚准备好的 id，用 parent() 方法，把画板填充到 id 标签中。
    ``` javascript
    let cav = createCanvas(width, height); 
    let p5Element = document.querySelector("#p5Element");
    cav.parent('p5Element');
    ```
![img](https://user-images.githubusercontent.com/20842136/133625684-60cccddb-e3a1-4225-84cd-410b918ff04b.png)
[测试代码_01](https://jsfiddle.net/niuuin/1jhe5xua/4/)

# P5js 画板尺寸
完成这些之后发现把事情想简单了，当通过 CSS 调整宽度时，P5js 画板会被挤压变形，画板内的元素也会产生形变。

在 CSS 文件中添加：

``` css    
canvas {
    max-width: 100%;
}

.content {
    width: 50%;
    margin: o auto;
}
```
![img](https://user-images.githubusercontent.com/20842136/133625776-901e0088-9a64-4304-b285-052c00701ab9.png)

在网页上出现这种问题，就代表不可用，我想 P5js 有没有相关方法能解决这个问题，找了半天也没找到，很沮丧，然后就去做别的事情了。

刚刚突然想到，也许不是 P5js 没有解决这个问题的方法，而是这事儿不归 P5js 管，马上去验证了一下，果不其然。

核心在于画板尺寸 `createCanvas(window.innerWidth, window.innerWidth * 0.4);`，当前使用的 `window.innerWidth` 返回文档显示区域宽度，也就是画板尺寸跟随文档显示区域变化。

当 CSS 调整宽度时（如：width: 50%;），不会影响文档显示区域，它只影像页面中的元素（画板就是元素之一），当我们用 `window.innerWidth` 定义画板宽度，再通过 CSS 调整元素宽度时，翻译过来就是在画板尺寸不变的基础上缩小 50%，`window.innerWidth` 和 CSS产生冲突，所以出现挤压、形变的问题。

我们要做到的是：不用 `window.innerWidth` 定义画板宽度，而是用元素的宽度，这样在 CSS 调整宽度时，画板尺寸会跟随 CSS 变化，而不是在原有尺寸的基础上缩放。

``` html
<div class="content">
  <div>123</div>
  <div id="p5Element"></div>
  <div>456</div>
</div>
```

``` javascript
let p5Element = document.querySelector('#p5Element');
let canvasWidth = p5Element.offsetWidth;
let p5Width = canvasWidth;
let p5Height = canvasWidth * 0.6;

function setup() {
  cav = createCanvas(p5Width, p5Height);
  cav.parent('p5Element');
}
```

``` css
 body {
   padding: 0;
   margin: 0;
 }

 .content {
   width: 90%;
   margin: 0 auto;
 }

 canvas {
   max-width: 100%;
 }
```
js 文件 `let canvasWidth = p5Element.offsetWidth;` 中的 [offsetWidth](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLElement/offsetWidth) 就是用来获取元素宽度的，用它来定义画板尺寸，这样的话无论在 CSS 中怎么调整宽度，画板尺寸都直接跟随 CSS 变化，而不是在原有基础上进行缩放。

![img](https://user-images.githubusercontent.com/20842136/133625877-614d6c7b-7883-45e0-ac23-920f8c0571f1.png)
[测试代码_02](https://jsfiddle.net/niuuin/evnmjfod/55/)

# 响应式
目前的状态还不支持响应式，这也是决定方案能否投入实际用途的关键问题。这事儿归 P5js 管，而且还很容易。

## windowResized
![img](https://user-images.githubusercontent.com/20842136/133625945-a1838983-f3c7-4709-91f7-0f00823e6333.png)
通过 [windowResized](https://p5js.org/zh-Hans/reference/#/p5/windowResized) 解决，我们需要在浏览器窗口缩放时：

``` javascript
function windowResized() {
    重新获取元素宽度；
    重新定义画板尺寸；
    重新设置画板尺寸；
}
```
![img](https://user-images.githubusercontent.com/20842136/133626029-7af96ca6-27ad-49e6-9c74-5569d7e53917.gif)
[测试代码_03](https://jsfiddle.net/niuuin/qysx3tvz/35/)

现在的状态完全支持 CSS 和响应式，已经可以投入到项目中了，如果你也遇到类似需求，在这个基础上写自己的内容就好，完全不用操心 P5js 之外的事情。

# 测试完了就动点真格的
![sketch_134_PunctuationCn_05_138](https://user-images.githubusercontent.com/20842136/133626157-614c8c6e-c93c-46e8-9f63-8f7840a3311c.png)

新作品《标点符号们》中，标点符号不断变化显现的部分是通过 Processing 输出的，也被我拿来当动态贴图，在整个作品中出镜率很高，做网站页面时本来放了上面这张图片，看来看去觉得差点意思，所以有了文章开头的想法。

![ezgif com-gif-maker (15)](https://user-images.githubusercontent.com/20842136/133626240-62984262-f653-41d9-82f6-1057c2cb8e6d.gif)

![Snipaste_2021-09-16_16-25-10](https://user-images.githubusercontent.com/20842136/133626328-abb172da-15a5-4d40-9bf3-04bab4b3a07f.png)

折腾了半天总算搞定了，现在已经成功地把 P5js 作为页面元素，置入到 HTML 结构中，并且支持 CSS 和响应式，你可以在 [很大声 Web - 标点符号们](https://hendasheng.com/works_page/punctuation.html) 体验，欢迎你来游玩：）