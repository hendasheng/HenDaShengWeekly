# 很大声周刊-vol.93
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

# Chladni - 克拉尼图案
![image](https://pub.mdpi-res.com/applsci/applsci-11-10094/article_deploy/html/images/applsci-11-10094-g005.png?1635855066)

## Houdini Vex Chladni - Entagma 
![image](https://user-images.githubusercontent.com/20842136/219848644-3d761896-3788-429c-9871-9c949658d4b5.png)

[Houdini Vex Chladni - Entagma](https://www.bilibili.com/video/BV1Pq4y147kG/?p=10&spm_id_from=pageDriver&vd_source=6c68891752436b0097051bf700e169a9)

## 【教程】用 houdini 制作程序化 Chladni 图案 - Clown_丑
![image](https://user-images.githubusercontent.com/20842136/219848509-d564103b-d380-42a0-9bfa-136f81a0dad1.png)

[【教程】用houdini制作程序化Chladni图案 - Clown_丑](https://www.bilibili.com/video/BV1P94y1o7Aq/?spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=6c68891752436b0097051bf700e169a9)

## 关于 Chladni 图案
![image](https://user-images.githubusercontent.com/20842136/219849399-b3fad1a6-afde-4c31-858b-732611ded9d1.png)

[关于Chladni图案](https://zhuanlan.zhihu.com/p/108448193)

# 在三维物体上使用 Chladni 图案
![image](https://user-images.githubusercontent.com/20842136/219850469-ea9e5b5b-2738-4ccb-87e2-060d8ea4f1f7.png)

教程中的案例都是在平面上实现克拉尼图案，同样的做法可以直接用在三维物体上。但如果以此控制三维物体的位置信息就不行了，图案只有 x、y 两个轴向，而三维物体有 x、y、z 三个轴向。

![image](https://user-images.githubusercontent.com/20842136/219850940-5bc82cf8-9403-48fa-9c9d-0fb3d8f7b79b.png)

``` C++
// @z_height 为克拉尼图案结果
@P += @z_height * @N * 0.2;
```

这种情况下可以结合法线达到理想效，相当于通过法线把两个轴向变成三个轴向。

## 法线

![image](https://user-images.githubusercontent.com/20842136/219851086-b4df3f74-272d-404d-bc61-2fdf8103d2d4.png)

法线在三维世界中是非常重要的数据，以前在 Blender 中知道法线的存在，但是没法主动调用，Houdini 好玩的点在于所有数据都可以拿来使用，这才有机会理解法线，它可以做很多事，比如上文提到的控制位置参数，还能控制旋转角度。

![image](https://user-images.githubusercontent.com/20842136/219851905-f46214c4-881c-45e5-90e5-44ae40daa1df.png)

甚至可以转换成速度值，在动态模拟中这一点很重要，很多打包好的功能其实都有法线的参与。

# Houdini 相机约束
![image](https://user-images.githubusercontent.com/20842136/219850574-1f2ea9a9-3c0e-4838-be86-d869b437eb6d.png)

[Houdini 相机约束](https://www.youtube.com/watch?v=mC_RbVg7xdk&list=LL&index=8)

在相机中添加约束模块，实现目标跟踪和运动路径。

# 新必应 - AI 搜索引擎
![image](https://user-images.githubusercontent.com/20842136/219845755-ae62e228-ac5a-4be5-a5d1-d218cd6e76ef.png)

[新必应 - AI 搜索引擎](https://www.bing.com/new)

新版还没开放，需要提前申请，更行 Edge 浏览器即可看到相关引导页面。

# 微软必应步子迈太大，聊天机器人是有个性还是扯淡？
![image](https://user-images.githubusercontent.com/20842136/219848037-13add39c-6915-4e5c-b386-8ddfab66a2ac.png)

[微软必应步子迈太大，聊天机器人是有个性还是扯淡？](https://www.huxiu.com/article/798060.html)

> 当年为了让人工智能人人可用，马斯克与奥特曼等共同创办了OpenAI。今天微软要把ChatGPT加持的搜索产品必应推向亿万用户，马斯克不安了，害怕了。
> 
> 一位名叫Jacob Roach的科技记者，在试用微软人工智能驱动的搜索引擎新必应(New Bing) 的体验后，写了一篇文章 《“我想成为人类”，我与微软机器人的聊天激烈而又令人不安》。
 

# When You Are Near - Carolina Liar
![image](https://user-images.githubusercontent.com/20842136/219849750-88b0a85b-7d94-4753-a9f1-302e4bc4393c.png)

