# 很大声周刊-vol.168

# Houdini 22 抢先看
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/houdini-22.png)

[Houdini 22 抢先看](https://www.youtube.com/watch?v=lFG1FIXBprc)


Houdini 的版本发布通常以 0.5 递进，这次直接从 21 过渡到 22，具体内容在本月 22 号发布。

## 针对高斯泼溅的支持
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/houdini-22-animGSplates.png)

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/houdini-22-animGSplates-rig.png)

我感兴趣的部分是看到高斯泼溅部分，应该是有针对性工具发布，包含对高斯模型的动态和绑定。

## COPs - 纹理合成
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/houdini-COPs.png)

整个演示过程多次看到 [COPs](https://www.sidefx.com/docs/houdini/nodes/cop/index.html) 的身影，在新版本中继续加强，看得出 SideFX 希望它深入地融入各个工作流程。

## UI 变化
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/houdini-22-UI.png)

Houdini 也扁平了。

# Houdini 自定义相机剔除
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/915_Cam_Frustum.png)

在复杂场景中，相机剔除可以极大减少非必要的计算量，只有进入相机视野的部分才会参与后续处理，视野之外的部分都会被跳过，尤其是复杂模拟，可以极大减少性能浪费。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/915_Cam_Frustum-ezgif.com-video-to-gif-converter.gif)

<details>
<summary>查看 Houdini VEX 相机剔除代码</summary>

``` C++
// Houdini Vex - 相机剔除
string cam = chs("camera");

// 只保留这三个控制参数
float view_scale = chf("view_scale");
float near_dist  = chf("near_dist");  // 开始距离
float far_dist   = chf("far_dist");   // 结束距离

// 自动读取相机参数
float focal    = chf(cam + "/focal");
float aperture = chf(cam + "/aperture");

int resx = chi(cam + "/resx");
int resy = chi(cam + "/resy");

float aspect = 1.777777;
if (resx > 0 && resy > 0)
{
    aspect = float(resx) / float(resy);
}

// 防止参数错误
view_scale = max(view_scale, 0.001);
near_dist = max(near_dist, 0.001);
far_dist = max(far_dist, near_dist + 0.001);

// 相机 transform
matrix cam_xform = optransform(cam);

// Houdini 相机通常朝本地 -Z 看
float fovx = 2.0 * atan((aperture * 0.5) / focal);
float fovy = 2.0 * atan(tan(fovx * 0.5) / aspect);

// 缩放视角
fovx *= view_scale;
fovy *= view_scale;

// 计算 near / far 平面尺寸
float near_w = tan(fovx * 0.5) * near_dist;
float near_h = tan(fovy * 0.5) * near_dist;

float far_w = tan(fovx * 0.5) * far_dist;
float far_h = tan(fovy * 0.5) * far_dist;

// 本地空间 8 个角点
vector local_pts[];

append(local_pts, set(-near_w, -near_h, -near_dist)); // 0
append(local_pts, set( near_w, -near_h, -near_dist)); // 1
append(local_pts, set( near_w,  near_h, -near_dist)); // 2
append(local_pts, set(-near_w,  near_h, -near_dist)); // 3

append(local_pts, set(-far_w, -far_h, -far_dist)); // 4
append(local_pts, set( far_w, -far_h, -far_dist)); // 5
append(local_pts, set( far_w,  far_h, -far_dist)); // 6
append(local_pts, set(-far_w,  far_h, -far_dist)); // 7

int pts[];

for (int i = 0; i < len(local_pts); i++)
{
    vector p = local_pts[i] * cam_xform;
    append(pts, addpoint(0, p));
}

// 创建封闭视锥体，法线朝外

// near face
int pr_near = addprim(0, "poly");
addvertex(0, pr_near, pts[3]);
addvertex(0, pr_near, pts[2]);
addvertex(0, pr_near, pts[1]);
addvertex(0, pr_near, pts[0]);

// far face
int pr_far = addprim(0, "poly");
addvertex(0, pr_far, pts[4]);
addvertex(0, pr_far, pts[5]);
addvertex(0, pr_far, pts[6]);
addvertex(0, pr_far, pts[7]);

// bottom face
int pr_bottom = addprim(0, "poly");
addvertex(0, pr_bottom, pts[0]);
addvertex(0, pr_bottom, pts[1]);
addvertex(0, pr_bottom, pts[5]);
addvertex(0, pr_bottom, pts[4]);

// right face
int pr_right = addprim(0, "poly");
addvertex(0, pr_right, pts[1]);
addvertex(0, pr_right, pts[2]);
addvertex(0, pr_right, pts[6]);
addvertex(0, pr_right, pts[5]);

// top face
int pr_top = addprim(0, "poly");
addvertex(0, pr_top, pts[2]);
addvertex(0, pr_top, pts[3]);
addvertex(0, pr_top, pts[7]);
addvertex(0, pr_top, pts[6]);

// left face
int pr_left = addprim(0, "poly");
addvertex(0, pr_left, pts[3]);
addvertex(0, pr_left, pts[0]);
addvertex(0, pr_left, pts[4]);
addvertex(0, pr_left, pts[7]);

s@name = "camera_frustum_cutter"; 

```
</details>

# MediaPipe Solutions - 实时机器学习
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/MediaPipe%20Solutions.png)
[MediaPipe Solutions](https://developers.google.com/edge/mediapipe/solutions/guide) 是 [Google AI Edge](https://developers.google.com/edge) 提供的一套实时机器学习解决方案文档，覆盖视觉、文本、音频和生成式 AI 等任务。

![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/MediaPipe%20Solutions-1.png)

MediaPipe Solutions 并不是很新的项目，以前有过尝试，但是效果不太好。最近正好又遇到相关需求，重新尝试发现体验好了很多。

# FFmpeg testsrc - FFmpeg 测试视频源
[FFmpeg testsrc](https://ffmpeg.org/ffmpeg-filters.html) 是 [FFmpeg](https://ffmpeg.org/) 内置的测试视频源，属于 lavfi / libavfilter 里的 source filter。它不需要输入视频文件，可以直接生成标准测试画面，用来检查视频处理链路是否正常。

下面是几个常用的测试样式：
### smptebars
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/ffmpeg-testsrc/smptebars.png)
标清 SMPTE 彩条测试图。主要用于检查基础颜色、亮度、对比度、色彩通道和视频链路是否正常。画面是静态标准彩条，适合做显示、编码、转码、播放器兼容性的基准测试。

### smptehdbars
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/ffmpeg-testsrc/smptehdbars.png)
高清 SMPTE 彩条测试图。相比 smptebars，它面向 HD 视频标准，包含更复杂的灰阶、色条和参考区域。适合测试高清工作流里的颜色还原、亮度范围、压缩损失和显示校准。

### testsrc
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/ffmpeg-testsrc/testsrc.png)
FFmpeg 经典测试源。画面包含彩条、圆形、网格、黑白块和时间/帧信息区域，通常用于检查分辨率、比例、运动编码、帧率、裁切、缩放和画面方向。它比 SMPTE 彩条更偏“综合视频测试”。

### testsrc2
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/ffmpeg-testsrc/testsrc2.png)
testsrc 的增强版测试源。图案更复杂，包含大面积色块、渐变、斜线和小块区域，更适合观察编码压缩、色度采样、边缘细节、渐变 banding、缩放和滤镜处理后的变化。相比 testsrc，它更偏向编码/滤镜压力测试。

# 小白兔白又白
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/IMG_2164.jpg)

另一位选手最近总是藏起来。

# Going Shopping - The Strokes
![img](https://hendasheng-web.oss-cn-beijing.aliyuncs.com/Weekly/vol.168/Going%20Shopping%20-%20The%20Strokes.jpg)
