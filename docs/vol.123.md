# 很大声周刊-vol.123
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/83add787-a427-4101-94cc-c52677529be4)

# 要写清数据类型啊 - Houdini RBD
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/bf510836-7aad-4069-b032-3608e622f16b)

周刊以来记录过很多关于数据类型的问题，这回在 RBD 模拟上又遇到了。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/99457cae-fadc-4360-a750-05442496092b)

```
if(@mops_falloff > 0.25) i@active = 1;
i@deforming = 1 - i@active;
```

首先通过 [Mops](https://www.motionoperators.com/) 设置衰减（@mops_falloff)，根据 `@mops_falloff` 值激活刚体。

![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/f27be274-00c4-400c-b91e-8004e7f6f86b)

接着通过 [point velocity](https://www.sidefx.com/docs/houdini/nodes/sop/pointvelocity.html) 设置速度值。

![ezgif com-video-to-gif (3)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/59add514-c85f-4cb4-b1ba-3dc8fab98a51)

最终通过 `@mops_falloff` 激活刚体，并为其添加速度值。

---

前面的代码中明确了数据类型，所以得到了正确的结果。刚开始并不是这样，我忘了写数据类型，结果是各种各样的问题。在知道问题原因后发现问题又觉得问题出的理所应当，顺便了解一下各个属性的作用和层级关系。

```
if(@mops_falloff > 0.25) i@active = 1;
@deforming = 1 - i@active;
```
![ezgif com-video-to-gif (4)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/2a76f8ed-8d1f-4c87-ae0a-5b3307dd2fe8)

激活了 `active` 属性，但 `deforming` 没有注明数据类型（`i@deforming`），这时 Houdini 会把这个属性的数据类型默认为浮点数，而在 RBD 模拟中，`@deforming` 为浮点数时不会起作用。

---
```
if(@mops_falloff > 0.25) @active = 1;
@deforming = 1 - @active;
```

![ezgif com-video-to-gif (5)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/332c2b78-cd59-4ce0-93e6-5cfd472f1cbe)

这次两个关键属性都没注明数据类型，所以完全不起作用，可证 Houdini RBD 模拟对浮点值属性不起作用。

---

```
if(@mops_falloff > 0.25) @active = 1;
i@deforming = 1 - @active;
```

![ezgif com-video-to-gif (5)](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/332c2b78-cd59-4ce0-93e6-5cfd472f1cbe)

在 `@active` 未激活，只有 `@deorming` 激活时，也没有作用，可见 `@deforming` 只有在 `@active` 激活的情况下才有效，在 `@active` 未激活时，无论如何 `@deforming` 都不会起作用。

# 小白兔白又白
![微信图片_20230917172843](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/7a8712f5-d476-4803-963a-394edb99bd5d)

![微信图片_20230917172844](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/385418eb-b2a2-4384-a925-bfc79b119231)

# skin in the game - Slowdive
![image](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/18293ee4-82ae-41bf-ab75-70ebbf291f52)
