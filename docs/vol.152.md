# 很大声周刊-vol.152
![Title_WeChat_152](https://github.com/user-attachments/assets/b7a22372-86be-4c6c-b708-15117b21b584)


# 妄图理解全世界的噪波 / 程序化纹理
## 程序化纹理
![image](https://github.com/user-attachments/assets/1129ae79-2bd7-4cc6-beb8-bbd94d611ebd)

[噪波（常用 Perlin noise）](https://www.wikiwand.com/en/articles/Perlin_noise) 在视觉工作流程中很常见，它的诞生就是用来模拟自然现象、纹理，云、雾、地形、自然表面都可以通过它来实现。

程序化纹理本质上就是通过各种噪波算法模拟物体表面，它通过计算生成、不依赖分辨率，也不需要储存图像数据，只保存算法参数，相比贴图来说极大节省了储存空间，动态纹理也带来了极大的灵活性，谁用了都说好，各家渲染器对它都有充分的支持。

![image](https://github.com/user-attachments/assets/95e04253-b5e3-4a09-a297-39af5cb31434)
Blender Cycles / Eevee

![image](https://github.com/user-attachments/assets/b0783f0d-8c0b-4485-b8fd-34e9736e37a6)
Red Shift

## 噪波 Max Msp
![image](https://github.com/user-attachments/assets/56cb0be6-cfc2-4849-aaf8-2c03526fc776)

前面只是在使用噪波，也不太知道具体是咋回事，直到在 Max Msp 里使用噪波，它可以很直观的呈现噪波到底是什么。

噪波是矩阵，矩阵在不同语境含义差别巨大，这里只是字面意思，就是格子×格子，足够多数量的格子且每个格子中有不同的值就组成了噪波，各个噪波算法的结果就是影响每个格子的值。

![image](https://github.com/user-attachments/assets/0fb59cc9-4953-4c21-95c5-b69b62f14151)
这是把每个格子的值映射到色值上（10 × 10）。

![image](https://github.com/user-attachments/assets/d722543c-6774-4f66-bcfd-5868345d990d)
这是足够多的格子（800 × 800）。

![20241013-171006-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/840fdcf4-abc0-45e4-9d51-f9ad4217c3fe)
除了视觉噪波还可以用来控制声音，把每个格子的值转换成 MIDI 信号，就变成了随机播放的声音片段。

文件 -> [01_Noise_Test.maxpat](../data/vol_152)

# UE5 - 在蓝图中控制后处理参数
![image](https://github.com/user-attachments/assets/bc9c6ef9-da28-4d50-b387-8525ee563f12)

> 后期处理效果（Post-processing effect）使美术师和设计师能够对影响颜色、色调映射、光照的属性和功能进行组合选择，从而定义场景的整体外观。要访问这些功能，可以将一种称为 后期处理体积（Post Process Volume） 的特殊类型的体积添加到关卡。可以放置多个体积来定义特定区域的外观，也可以将其设置为影响整个场景。

![image](https://github.com/user-attachments/assets/78515728-0baa-46bc-b7cc-edfd2b5e7a1c)
[Changing Post Process Volume settings](https://www.youtube.com/watch?v=cZsCqWqFh8Q&t=128s)

非常简洁的视频教程，不过完全按照视频中的方式设置有一定问题，当 PostProcessVolume 有多个调整参数时，蓝图中修改任意参数后，其它参数都会变成默认设置。

搭配这个[（UE4 Управление Post Process volume через Blueprint）](https://www.youtube.com/watch?v=nR5i0xNCocI)服用效果更佳，里面的另一个方法可以解决上面遇到的问题。

具体方法是把 `Make PostProcess Settings` 替换为 `Set members in PostProcessSettings`，就可以实现控制参数变化时，其它参数不受影响。

具体原理我还没弄明白，但可以切实解决问题。

# UE5 在序列帧中触发蓝图事件
![image](https://github.com/user-attachments/assets/27a4f67d-aa81-41db-ada5-c71b577cd5d2)

[UE5 在序列帧中触发蓝图事件](https://www.youtube.com/watch?v=z09mAi92p4k&t=465s)

展示交互程序的时候可以通过录屏完成，因为实时交互的原因，画面质量不会很好，从追求画面质量的角度看，这事儿还是得离线渲染来办，这份教程讲解了如何在序列帧中触发蓝图事件，在录制演示视频得时候很好用，可以尽可能地提高画面质量。

# Ableton Move - Ableton 最新发布的硬件设备
![image](https://github.com/user-attachments/assets/e8a6a8cf-ed29-4e94-84c9-89a2b642fd8c)

![image](https://github.com/user-attachments/assets/2be19b0d-1e61-4a6e-ab50-ef35bd8297c0)

> [Ableton Move](https://www.ableton.com/zh-cn/move/) 可帮助您随时捕捉最佳创意。拿起它，寻找新的声音，并快速决定当下最合适的声音。跟随您的直觉，无论它会引领您到哪里。

# 小白兔白又白
![微信图片_20241013180703](https://github.com/user-attachments/assets/caec8572-badd-4c08-b278-e89173070c35)

![微信图片_20241013180654](https://github.com/user-attachments/assets/ca15945f-9ad9-4da1-b18e-1d80d8d6ac25)

# Goodnight Moon - Boogie Belgique
![image](https://github.com/user-attachments/assets/ccac6f3b-4d3d-413a-b8be-a00c7b0780dc)
