# 很大声周刊-vol.116
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_116 1](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/943eb5a1-c86f-49be-b412-391efdb19ecb)

# 自定义衰减控制激活刚体 - Houdini
![ezgif com-optimize](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/dde98a43-5e8b-42dd-b011-281294588f9a)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/68b2f17f-0241-4d87-b597-f5f0ad28ec00)

主要用到 `@acitive\@deforming` 两个影响刚体的属性。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/24ff5889-0d61-40ae-ab45-d9cfa3528257)

这两个属性可以通过 [RBD Configure](https://www.sidefx.com/docs/houdini/nodes/sop/rbdconfigure.html) 节点更直观地进行测试。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/749076e5-6c73-4061-b294-44a07165876c)

这里控制衰减用到的 [MOPs 模块](https://www.motionoperators.com/)，是开源第三方插件，需要提前安装，可以更轻松、直观地控制衰减值，从而影响目标属性，比如 `@acitive\@deforming`。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d109d900-d156-413d-b2c8-db19a3b41df5)

```C++
if(f@mops_falloff > 0.2) i@active = 1;
i@deforming = 1 - i@active;
```
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2cd42570-408f-4587-9a33-190045d4e5bd)

示例中的 `@v 速度` 值也通过自定义完成，只作用于 y 轴。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/d03b1a57-a174-491b-a681-60b210d99f7d)

在后面为它添加噪波，使得速度值更加自然。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/a4803432-2633-4ad9-a03c-546453eee476)


在这里也可以通过 [Point Velocity](https://www.sidefx.com/docs/houdini/nodes/sop/pointvelocity.html) 节点完成。

# Photo Mosh - 故障化处理（图片、视频）
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/8f4db2f2-f655-4ebf-b005-ca3410f756e7)

[Photo Mosh - 故障化处理（图片、视频）](https://photomosh.com/)

# Git Clone 下载文件的时候出现连接超时
```
//“1080” 替换成你的电脑端口数字
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy http://127.0.0.1:1080
```

# 刀郎《罗刹海市》/《山歌寥哉》是好音乐吗？中国音乐到底应该如何发展？- 叨叨冯聊音乐
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/658f2aa2-1714-41bd-b7c7-5472bb6d520b)

[刀郎《罗刹海市》/《山歌寥哉》是好音乐吗？中国音乐到底应该如何发展？](https://www.bilibili.com/video/BV1Y841127j6/?spm_id_from=333.880.my_history.page.click&vd_source=6c68891752436b0097051bf700e169a9)

# 小白兔白又白
![微信图片_20230730173500](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b77d985c-fb0a-4e86-a3dc-79522bf41641)
![微信图片_20230730173501](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/77592bff-3598-46d0-b3af-105c7d1e4fb5)
![微信图片_20230730173459](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/a8fd40d6-f651-42f8-851c-c0cb5532cc26)

# Heartbreak Summer(feat.K.Flay) - K.Flay/RAC
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2fe86958-547e-43e8-8ffd-ff5c8a4e1cf0)
