# 很大声周刊-vol.19
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![sketch_139_HenDaShengWeekly_vol-19_02_615](https://user-images.githubusercontent.com/20842136/132932990-48281785-2692-421b-b08a-0ccc56cf08d4.png)

![img](https://user-images.githubusercontent.com/20842136/132932999-e66993ee-9249-47c4-91ee-940478bdff2c.png)

[《设计师如何拥有自己的个人网站（一）》](https://sspai.com/post/68670)， 在少数派 Martix 社区发布的第一篇文章，聊了聊自己做个人网站的经验，希望对类有似想法的朋友有一定帮助，稍后会同步到公众号中。

# bricklayer.js
![image](https://user-images.githubusercontent.com/20842136/132934046-dbc52ee9-d691-4fe9-b270-0eb122de2ac3.png)

[bricklayer.js](https://github.com/ademilter/bricklayer) 是一个轻量级瀑布流布局库。

[很大声 Web 2.0](https://hendasheng.com/) 中的瀑布流布局就用到了 beicklayer.js，配置非常简单，几乎是开箱即用（[测试代码](https://jsfiddle.net/niuuin/pho1bfy8/2/)）。

![image](https://user-images.githubusercontent.com/20842136/132934176-6f99ace1-134e-4360-87e2-c96c9567e33e.png)

![image](https://user-images.githubusercontent.com/20842136/132934235-870114a0-6d2c-4101-88d8-4554ad11c04b.png)

在这之前瀑布流布局用到的是 [Masonry.js](https://masonry.desandro.com/)，也挺好用的，可是在 Firefox 上出现 bug，所有元素都堆叠在一块。

> [Masonry 不支持 Flex Box CSS](https://github.com/desandro/masonry/issues/1053#issuecomment-405022401)
> ![image](https://user-images.githubusercontent.com/20842136/132118011-b7671f73-1d0a-4156-a688-7152dcf716b8.png)

后来发现是它不支持 Flex 布局，而我偏偏用到的就是 Flex 布局，所以把瀑布流布局库换成了 [bricklayer.js](https://github.com/ademilter/bricklayer)。 

# CSS 实现瀑布流布局
目前实现瀑布流布局需要借助 js 的帮助，上面提到的瀑布流布局库都有 js 参与。

在解决瀑布流布局问题的过程中，还发现一些好玩的事情。

## CSS columns
[CSS columns](https://developer.mozilla.org/zh-CN/docs/Web/CSS/columns?continueFlag=f2aeadc6d507ff1e919e27925b7e4d4a) 用来设置元素的列宽和列数。

![img](https://user-images.githubusercontent.com/20842136/132934841-74d6c76d-8215-499e-8063-d227f67a199e.png)
它可以轻松“实现”瀑布流布局，网络上有好多类似“CSS 实现瀑布流”这样标题的文章都是这种方法，确实能实现，但几乎没有实用价值，因为排列顺序，它只能先纵向后横向排列（上图），这也符合它原本的功能逻辑，可是通常我们需要的瀑布流布局是这样先横向后纵向的排列（下图）。
![img](https://user-images.githubusercontent.com/20842136/132934893-1f7276e1-d8c0-444f-b55b-cc8c27e3c0af.png)
CSS columns 做不到这样，相别的办法吧。

## grid-template-rows: masonry
![image](https://user-images.githubusercontent.com/20842136/132934997-4a6ca180-c2cb-4a79-a9a9-4ba716f22fc9.png)
[grid-template-rows: masonry](https://www.smashingmagazine.com/native-css-masonry-layout-css-grid/?continueFlag=f2aeadc6d507ff1e919e27925b7e4d4a) / [Masonry Layout MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Masonry_Layout)，这就是为瀑布流布局而生的 CSS 属性，基于 [CSS Grid 布局](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)，可是目前还没得到全面支持，只能在 Firefox 实验功能中实现，希望这个属性尽快被全平台支持，以后瀑布流布局只用 CSS 就能实现了。

# Blender 背面材质
![Snipaste_2021-09-11_11-49-15](https://user-images.githubusercontent.com/20842136/132935430-9a1e82a1-c99a-4d3c-bf76-8e1ecbb5ea0d.png)

通过 `UV 映射 + 几何数据（背面）` 实现平面正反面两种。

# Erindale 的针织材质教程
![Snipaste_2021-09-11_11-53-22](https://user-images.githubusercontent.com/20842136/132935512-1e2a6d55-95e0-4154-abaa-0b83beb5c5d1.png)

和他的节点教程一样，让人眼花缭乱，属于那种看着特别吃力但很过瘾的类型，作者对各个节点的理解让人羡慕。

![Snipaste_2021-09-11_11-55-25](https://user-images.githubusercontent.com/20842136/132935649-1062c36e-f2e6-40ab-a5e3-1551aaa2ad14.png)
Blender 2.93 的欢迎画面就出自 [Erindale](https://www.youtube.com/watch?v=yo54Tp9a3lI&t=65s) 之手。

# 少数派 Matrix 社区
![image](https://user-images.githubusercontent.com/20842136/132935716-6f172b7c-e013-4487-97fb-d37cb59e14e8.png)

[Matrix](https://sspai.com/matrix) 是 [少数派](https://sspai.com/) 旗下的写作社区，偏向数字、科技类内容。

我的文章都发布在自己的公众号上，在此之外一直想找一个更垂直、更细分的平台发布，Matrix 社区是个不错的平台。

