# 很大声周刊-vol.127
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Alt text](image-16.png)

# Houdini 输出点云文件 .ply 到 Touchdesigner
![img](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/464ce2bd-d30b-4c41-83a6-42acfc0cb4d1
)

## 准备模型
![Alt text](image-4.png)
![Alt text](image-3.png)

## 输出点云文件 .ply
![Alt text](image-5.png)

## 模型转点云 - VEX
![Alt text](image-6.png)

``` C++
// keijiro
// https://gist.github.com/keijiro/4aa156ac21779dcdc85849062785db2f

int vlist[] = pointvertices(0, @ptnum);
vector uv = vertex(0, "uv", vlist[0]);

string path = "texture_file_path.jpg";
@Cd = colormap(path, uv);
```
![Alt text](image-8.png)

方法来自 [mesh_to_pointcloud - keijiro ](https://gist.github.com/keijiro/4aa156ac21779dcdc85849062785db2f) 

![Alt text](image-7.png)

## 输出点云文件 .ply
![Alt text](image-9.png)

通过 [ROP Geometry Output](https://www.sidefx.com/docs/houdini/nodes/sop/rop_geometry.html) 输出 [.ply](https://www.wikiwand.com/en/PLY_(file_format)) 文件。

## 在 Touchdesigner 中读取 .ply
![Alt text](image-11.png)
颜色信息

![Alt text](image-12.png)
转换 RGB

![Alt text](https://github-production-user-asset-6210df.s3.amazonaws.com/20842136/275225936-df116263-6eb2-4596-afe8-bd175c48bb9a.gif)

# 小白兔白又白
![Alt text](image-17.png)
![Alt text](image-18.png)

# Beyond Beliefs - Ben Böhmer
![Alt text](image-15.png)