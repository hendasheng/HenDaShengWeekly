# 很大声周刊-vol.158 | Blender Python + OSC 实时切换相机
![Image](https://github.com/user-attachments/assets/fd4314f0-1f56-4591-899e-2a5b1bb46b3c)

[NodeOSC](https://github.com/maybites/NodeOSC?tab=readme-ov-file) 是 Blender 上非常好的用的 OSC 插件，能满足大多数需求。

![Image](https://github.com/user-attachments/assets/1f67c5fd-2112-4ef3-a474-9a8c1799d736)

启用 NodeOSC 插件后，在参数右键菜单中会出现 `Create a node osc handler` 选项，用来创建对应的 OSC 接口，这意味着只要有这个选项的参数都可以被控制。

可是相机切换并没有这个选项，也就没办法创建 OSC 接口，这就是“满足大多数需求”之外的需求，我想通过 OSC 控制相机切换，只好尝试自己动手实现。

![Image](https://github.com/user-attachments/assets/dfd978ef-e019-466f-8d3a-dc4bd00b6265)

这种情况当然需要 AI 工具的帮助，它大幅降低了编程的门槛，但是并没有把这个门槛彻底干掉，需要自己解决这个问题时要对 python / OSC 有基本的了解，我对“基本”的理解是能完整、清晰地提出问题，并且知道程序基本运行原理就好。


“我需要获取场景中所有相机，并且根据 OSC 信号切换不同的相机，比如 `1 -> 第一个相机 / 2 -> 第二个相机  ...`”


> 明白了！你想要在 Blender 中通过 OSC 消息切换场景中的不同相机。下面是完整的代码修改版本，它将在收到 OSC 消息后解析数字，并将当前场景的激活相机切换为对应编号的相机：
> 
> ✅ 功能概述：
> 检测当前场景中所有相机对象；
> OSC 接收到如 "/osc/camera 1" 的消息时，切换到第 1 个相机；
> 支持无限数量相机，只要是 bpy.types.Object 且 obj.type == 'CAMERA'。

``` python
import sys
sys.path.append(r"C:\Users\lnlao\Desktop\BlenderPythonLib")

import bpy
from pythonosc import dispatcher
from pythonosc import osc_server
from pythonosc import udp_client
import threading

# OSC 客户端（用于发送相机数量）
osc_client = udp_client.SimpleUDPClient("127.0.0.1", 6000)  # 修改为接收端的地址和端口

# 获取所有相机对象
def get_cameras():
    return [obj for obj in bpy.data.objects if obj.type == 'CAMERA']

# 设置当前激活相机
def switch_camera(index):
    cameras = get_cameras()
    if 0 <= index < len(cameras):
        bpy.context.scene.camera = cameras[index]
        print(f"Switched to camera: {cameras[index].name}")
    else:
        print(f"Invalid camera index: {index}")

# 处理 OSC 消息（切换相机）
def osc_handler(address, *args):
    if args:
        try:
            cam_index = int(args[0]) - 1  # 输入1表示第0个
            switch_camera(cam_index)
        except ValueError:
            print("OSC argument is not an integer")
    else:
        print("No OSC argument received")

# 启动 OSC 服务器
def start_osc_server():
    ip = "127.0.0.1"
    port = 5005  # 接收端口

    disp = dispatcher.Dispatcher()
    disp.map("/osc/camera", osc_handler)

    server = osc_server.ThreadingOSCUDPServer((ip, port), disp)
    print(f"OSC Server started on {ip}:{port}")
    server_thread = threading.Thread(target=server.serve_forever)
    server_thread.daemon = True
    server_thread.start()

# 主函数
def main():
    cameras = get_cameras()
    print(f"Found {len(cameras)} camera(s)")

    # 启动服务器
    start_osc_server()

    # 向另一个端口发送当前相机数量
    osc_client.send_message("/osc/camera_count", len(cameras))
    print(f"Sent camera count to port 6000: {len(cameras)}")

main()
   
   
```

看注释基本能明白个大概，有几个地方需要注意：

``` python
import sys
sys.path.append(r"C:\Users\hendasheng\Desktop\BlenderPythonLib")
```
这个 Blender 引入外部库的基本方式之一。

<br>

``` python

def start_osc_server():
    ip = "127.0.0.1"
    port = 5005  # 接收端口

    disp = dispatcher.Dispatcher()
    disp.map("/osc/camera", osc_handler)
    ...
```

这里是 OSC 通信的核心参数，接收 / 发送端在这三个核心参数精确匹配的情况下才能正常通信。

**IP（Internet Protocol 地址）** 
表示信号要“送到哪台设备”；
在同一台电脑上运行多个程序时，常用 127.0.0.1（localhost）；
如果是两台设备间通信，则需要填写目标设备在局域网中的真实 IP；

**Port（端口号）**
表示信号“发到设备的哪个入口”；
每个监听 OSC 的程序会监听一个特定端口（如 5005、6000）；
发出端必须把数据“发送”到这个端口，接收端才能收到；

**Address（地址字符串）**
类似于 API 路径，是对数据“类型”的标识。

通常是自定义的字符串，如：
/osc/posx
/osc/rotx
发出端和接收端必须一致，否则接收端会忽略该消息。

![Image](https://github.com/user-attachments/assets/51d345cb-50da-45d0-b0e0-efbcd9bc1f4f)

这一步 Blender 部分就完成了，有一个猴头和多个相机，通过 python 创建了 OSC 服务器，以 5005 端口接收信息，其中地址为 /osc/camera 的信号控制切换到哪个相机。
<br>

```python
osc_client = udp_client.SimpleUDPClient("127.0.0.1", 6000)
```

代码中还有一点更便捷的处理，在获取场景中相机数量后，将数量发送到 6000 端口，地址为 /osc/camera_count。
<br>

![alt text](https://github.com/user-attachments/assets/5394e9a3-0249-4163-bdd7-ebcbe7e7d686)

发送端以 MaxMsp 为例：
- 先通过 6000 端口接收相机数量，用来控制最大随机值（左上）；
- 每秒更新一次随机值（右） ；
- 将随机值也就是相机编号通过 5005 端口发送到 Blender（左下）；

![Image](https://github.com/user-attachments/assets/fd4314f0-1f56-4591-899e-2a5b1bb46b3c)

最终实现了通过 OSC 控制相机切换的需求，[MaxMsp](https://cycling74.com/) 需要多说一句，它可以实现更复杂更自动化的信号控制，对于实时项目来说是非常好的工具。