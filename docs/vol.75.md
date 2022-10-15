# 很大声周刊-vol.75
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_75](https://user-images.githubusercontent.com/20842136/195976659-f2f3b0d2-ca03-4b4e-aa47-9fc4078ec518.png)

# Houdini VEX noise 写法
![ezgif com-gif-maker](https://user-images.githubusercontent.com/20842136/195977069-4b8dd3db-251e-4b0e-970c-790c9bc04514.gif)

中间遇到些问题，在论坛中也得到了一定的解答，上方是目前的效果。

**[关于 VEX 噪声方向偏移问题 - 论坛](https://www.sidefx.com/forum/topic/86836/?page=1#post-375167)**

![image](https://user-images.githubusercontent.com/20842136/195976957-653de17e-f8a9-4312-ab7f-2e8b26367879.png)

``` C++
vector freq = chv("freq");
vector off = chv("freq_off");
vector amp = @Cd.r;
float rough = chf("rough");
float atten = 1;
float turbulence = chf("turb");

vector mult_height = chv("mult_height");
vector active_v = anoise(v@P * freq + off, turbulence, rough, atten);

active_v = fit(active_v, 0, 0.5, -1, 1) * amp * mult_height;

v@P += active_v;
v@P.y += mult_height.y;

v@Cd = fit01(v@P.y, 0, 1);

@pscale = chramp("scale", @Cd.r) * chf("scale_mult") * 0.02;
v@Cd = chramp("color",v@P.y);
```

# 关于 Houdini VEX
Houdini VEX 是跳过节点直接操作数据的方式，它更灵活、更可控，但是灵活、可控的程度和代码编写的难易度成正比，现有的节点就可以理解成是一个个封装好的 VEX 模块，不同节点解决不同需求，当遇到节点不能覆盖的需求时就只能通过 VEX 解决了。

我在尝试过程中发现以前写 [Processing](https://processing.org/) 的经验对这学习 VEX 很有帮助，如果你觉得 VEX 难以理解，或许可以尝试先玩一玩 Processing，它足够轻便，可以帮你解决数据类型、循环、函数、条件判断等等大多数编程概念。

# 自定义 Processing 配色方案
![image](https://user-images.githubusercontent.com/20842136/195977592-bfcc0829-8382-4b5b-a23d-ea7805e83766.png)

新版本的 Processing 包含多种配色方案，可是在众多方案中，内容区域也只有黑、白两种颜色，好看好玩当然很重要，可是易用性也不能不考虑，这么黑的背景色对眼睛并不友好，在日常使用各种应用的时候也不难发现，深色模式更多是不同程度的深灰色，好在 Processing 在配色方案这件事上彻底放开了，在包含众多配色方案的同时，还支持[自定义配色](https://discourse.processing.org/t/processing-4-change-editor-window-colour/31717)，按需编辑配置文件就好。

![image](https://user-images.githubusercontent.com/20842136/195977895-8a9599e2-30e7-43de-be65-f7b8c62281fe.png)

配置文件是一个 txt 文档，VS Code 可以帮你更方便的完成这件事，在 VS Code 上安装 [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight) 插件，可以高亮显示色值，便于观察。

![image](https://user-images.githubusercontent.com/20842136/195978471-395c3fb9-d7a3-4d49-86c1-9051cd0862f8.png)

理想状态应该是高亮显示色值并且可以编辑色值，但目前还做不到，没有针对 txt 文件的选色器，有一个迂回的办法，可以在 css 文件中编辑色值，确定好配色后，再将色值粘贴到 Processing 配色文件中即可。

![image](https://user-images.githubusercontent.com/20842136/195978692-c8088b2a-6efe-4255-8c98-42b477f1002e.png)


# DIORIVIERA 限定系列 - Web 3D
![image](https://user-images.githubusercontent.com/20842136/195978874-1d2f5292-5628-42ca-95c1-4ba40a4b64cc.png)

迪奥 [DIORIVIERA 限定系列](https://capsule.dior.cn/dioriviera-2022/)，通过 [Three.js](https://threejs.org/) 实现 Web 端 3d 场景。

逛一圈下来有点晕啊。

# Blender 驱动器限制映射值表达式
![image](https://user-images.githubusercontent.com/20842136/195979086-deaf21de-dc1b-4099-bfca-3bfaec106359.png)

``` Python
radians(var*60) if (radians(var*60) < radians(90) ) else radians(90)
```

前几期聊过驱动器表达式，最近又遇到了需要驱动器的地方，同样是条件判断，用来限制被驱动物体的旋转角度。

[Blender 几何节点](https://docs.blender.org/manual/zh-hans/dev/modeling/geometry_nodes/introduction.html)推出后就很少用到[驱动器](https://docs.blender.org/manual/zh-hans/dev/animation/drivers/drivers_panel.html)了，但是有些时候还非它不可，了解一下准没错。

# 小白兔白又白
![9AD27AEF-9C8E-49C2-A3DC-A36985F976CE](https://user-images.githubusercontent.com/20842136/195980374-200373dc-9d40-4504-9c3c-09f2b8bc7000.jpeg)
![72008C38-9CF2-4D57-AFE3-E60CD998496B](https://user-images.githubusercontent.com/20842136/195980369-805eea25-4d5a-4541-ac8a-538b649c1d6a.jpeg)
![FAC7478C-641D-4A3F-8D0F-F60CD9AAD55C](https://user-images.githubusercontent.com/20842136/195980371-233f2ec3-621c-4122-85f4-db29d1e1d87a.jpeg)
![71651753-3997-4E9B-B35A-92148B3FCF2F](https://user-images.githubusercontent.com/20842136/195980376-a7c3312f-ebfc-4f8a-a847-e00234551e58.jpeg)

# 后互联网时代的乱弹 第34期
<img width="945" alt="image" src="https://user-images.githubusercontent.com/20842136/195996108-331f3125-3ec1-4bd5-be83-dd7e9f8dda72.png">

**[后互联网时代的乱弹 第34期](https://www.bilibili.com/video/BV1WG4y1p7Zw/?spm_id_from=444.41.list.card_archive.click&vd_source=6c68891752436b0097051bf700e169a9)**

# 别来无恙 - 简约情人
![10B8E9B2-1968-4E9D-9AC3-3BEE3A07A891](https://user-images.githubusercontent.com/20842136/195980372-1377e5c8-2b23-4811-9a90-b0299510ba45.jpeg)
