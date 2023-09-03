# 很大声周刊-vol.121
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_121 1](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/7050583f-a8bc-4c17-a191-7f8eb764d698)

# Houdini Copy To Points 稍复杂一些的用法
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/be3807cb-6c38-4b8a-a85d-3fd2ef92dee8)

[Copy To Points](https://www.sidefx.com/docs/houdini/nodes/sop/copytopoints.html)

## 多个物体复制到点
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b6fb507f-2aca-431c-9b02-19d83addb745)

通过 [attribfrompieces](https://www.sidefx.com/docs/houdini/nodes/sop/attribfrompieces.html) + [name](https://www.sidefx.com/docs/houdini/nodes/sop/name.html) 属性。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/4ec6b8fe-7e71-4f55-9418-5f0778e4293c)
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b342c61d-9429-42ca-8c8c-a24fca857a96)
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/569c22f7-09a0-4bcf-900e-85409a0ad64d)

相当于给每个物体取个名字，用 `attribfrompieces` 拆分后把 name 属性传递到 CopyToPoints 中。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2695f981-a3f4-4db8-a668-6fbf62e3c3f1)

![ezgif com-video-to-gif (1)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/c387f805-9bbe-4551-bac5-896183d38553)

[attribfrompieces](https://www.sidefx.com/docs/houdini/nodes/sop/attribfrompieces.html) 中附带多种分配模式供选择。

## 控制物体数量比重
在上面例子中增加 `attribrandomize`，这个节点我经常用它控制颜色或缩放，最近发现它可以自定义分布。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/e02f0547-18bd-4659-b83b-3134bfa187df)

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/50924c42-6941-4170-8508-e73d77fd802f)

![ezgif com-video-to-gif (2)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/0d788935-bda7-40c5-b072-ddc55585e311)

这样就正好可以把上面定义过的 `name` 属性拿来，通过这种方式，控制不同物体的权重值。

## MOPs Instancer
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2098279d-7de7-4433-878a-44a691bcd978)

更简单的办法是通过 [MOPs](https://www.motionoperators.com/) 插件的 [MOPs Instancer](https://github.com/toadstorm/MOPS/wiki/MOPs-Tutorial-4:-Creating-Instances) 模块完成，除了这种实例化的需求，MOPs 还提供了很多可以简化操作的实用功能。

# 小白兔白又白
![微信图片_20230903162428](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/54294fa0-ed65-45e7-85fc-ff513754101b)
![微信图片_20230903162430](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/ab8f583a-149f-46d0-ae7c-778d5ffca76c)

# Perfect Past - Molly Nilsson
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/b8883a1f-1616-460a-a00c-72551229508f)

