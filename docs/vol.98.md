# 很大声周刊-vol.98
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_98 1](https://user-images.githubusercontent.com/20842136/227722688-5fd72219-565e-4606-8aa1-5e2bf5c40b95.png)

# Houdini Vex 获取点数量 @numpt
![image](https://user-images.githubusercontent.com/20842136/227714682-7dfa3234-d543-4ded-b869-ae46c3d9e01b.png)

``` C++
int pointCount = @numpt;
@pointCount = pointCount;  // 将变量传输到外部（显示在数据表格中）
```

# Houdini Vop 获取点数量 Point Count VOP node
![image](https://user-images.githubusercontent.com/20842136/227714606-216d7317-4f2d-4339-8c2b-157f1c4e1383.png)

[Point Count VOP node](https://www.sidefx.com/docs/houdini/nodes/vop/npoints.html)

# Houdini Vex 获取面数量 @numprim
![image](https://user-images.githubusercontent.com/20842136/227714823-ed80e3c1-57d3-483a-ae78-8011d2eac117.png)

``` C++
int primCount = @numprim;
@primCount = primCount;
```

# Houdini Vex 获取面编号 @primnum
![image](https://user-images.githubusercontent.com/20842136/227714945-678dcf41-9327-4019-b0c3-812d332c6aab.png)

``` C++
int primNum = @primnum;

@primNum = primNum;
```

# 这些可以干嘛？
![image](https://user-images.githubusercontent.com/20842136/227715316-12d9d148-401e-4e4e-8d93-92ef5dfe9649.png)

比如想在一大堆平面中根据点/面数量或编号做针对性处理。

![image](https://user-images.githubusercontent.com/20842136/227715548-de62b2ec-21e4-4d5f-a062-ac79b30102f2.png)


``` C++
int pointCount = @numpt;
if(pointCount <= chi("Count")) removepoint(0, @ptnum);
```


# UE 导入 FBX 模型无法读取顶点颜色怎么办？
![image](https://user-images.githubusercontent.com/20842136/227708774-1fa351e6-d11f-4bc8-8e82-6d968687b928.png)

[FBX 无法导入顶点颜色 - UE Forums](https://forums.unrealengine.com/t/fbx-not-importing-with-vertex-colours/458342)

![image](https://user-images.githubusercontent.com/20842136/227715296-d485b3c5-c264-47d1-abc4-6eeeb5c8f3f0.png)

FBX 导入选项中「顶点颜色导入选项」选择「替换」即可导入顶点颜色，在材质中通过「VertexColor」节点引入。

# 小白兔白又白
![微信图片_20230325221455](https://user-images.githubusercontent.com/20842136/227722640-dfb5499a-1c05-4f28-b0a3-61344476e0c7.jpg)
![微信图片_202303252214551](https://user-images.githubusercontent.com/20842136/227722643-aba77a0d-bb8c-4733-bc99-34ab594d4df2.jpg)

# Dirty Town - Mother Mother
![image](https://user-images.githubusercontent.com/20842136/227722291-41b8fed4-c15d-458f-85f8-61ca6109c95e.png)
