# 很大声周刊-vol.154

#  osc in p5.js - 通过 p5js 收发 OSC 信号
[osc in p5.js](https://github.com/genekogan/p5js-osc) 基于 [osc-web](https://github.com/automata/osc-web) 的 p5js osc 收发方案。

![image](https://github.com/user-attachments/assets/557835b3-34cb-4900-83e6-1ce25a99c72a)

文档中的说明写的简洁、清晰，但对只接触过 p5js 的朋友来说有点不太好理解，所以我在这梳理一下每一步都在干嘛。

**所有操作均在 `终端` 中执行。**

## Install node
![image](https://github.com/user-attachments/assets/d306c113-fda5-447a-a064-053d062f0a8a)

p5js 可以理解为是一个偏向视觉、交互的 JavaScript（js）库，底层还是 JavaScript。

JavaScript 只能运行在浏览器端，但是有些情况下需要一些功能在服务器端运行，比如连接 osc 信号的应用。

[Node.js](https://nodejs.org/zh-cn) 解决的就是这个问题，它是一个全局 js 运行环境。

## git clone
![image](https://github.com/user-attachments/assets/3231f2f8-e85e-44eb-866a-2a41f3d3976e)

`git clone` + `仓库地址` 是把仓库下载到本地的 [git](https://git-scm.com/) 命令。

[git](https://git-scm.com/) 是运行在本地的版本控制工具，搭配 [GitHub](https://github.com/) 可以更高效地管理代码/仓库。
- `git status` - 检查状态；
- `git add .` - 将所有改动添加到暂存区，准备提交；
- `git commit -m "Modify Content"` - 改动注释；
- `git push -u origin master` - 将改动提交到仓库；


[Git 和 GitHub 简明入门 - soulhacker](https://www.bilibili.com/video/BV1LE411a7dY/?spm_id_from=333.999.0.0&vd_source=6c68891752436b0097051bf700e169a9)

## cd p5js-osc
当 p5js-osc 下载到本地后，前往 p5js-osc 文件夹，`cd` 指的是 `前往`。

## npm install
安装所有文件中的所有依赖项

一个文件中包含很多依赖项，这些依赖项通常不会放在仓库中，而是通过一个叫 npm 的工具自动管理。

![image](https://github.com/user-attachments/assets/f35d9d4b-2e6c-4b33-b514-a1f4f114fea4)

 [npm](https://www.npmjs.com/) 是 NodeJS 默认的包管理器，项目的依赖项会被记录在自动生成的 package.json 文件中。

 ``` js

// package.json
...
  "dependencies": {
    "@emotion/react": "^11.11.1",
    "@p5-wrapper/react": "^4.4.2",
    "@react-hook/media-query": "^1.1.1",
    "@react-three/drei": "^9.96.1",
    "@react-three/postprocessing": "^2.15.12",
    "gsap": "^3.12.5",
    "lazysizes": "^5.3.2",
    "p5": "^1.9.0",
    "react": "^18.2.0",
    "react-awesome-reveal": "^4.2.7",
    "react-dom": "^18.2.0",
    "react-fast-marquee": "^1.6.5",
    "react-ga4": "^2.1.0",
    "react-router-dom": "^6.26.1",
    "react-type-animation": "^3.2.0",
    "vite-plugin-glsl": "^1.2.1",
    "vite-plugin-svgr": "^4.2.0"
  },
  ...
 ```

 下载项目后，执行 `npm install` 后，它会根据这个 json 问价自动下载并安装这些依赖项。

 ## node bridge.js
 ![image](https://github.com/user-attachments/assets/af19a478-7301-42eb-a49c-08cc62a1e919)

 启动 `bridge.js` 文件，它的作用在于通过 [WebSocket](https://developer.mozilla.org/zh-CN/docs/Web/API/WebSockets_API) 与浏览器建立连接，这样 p5.js 就可以发送和接收数据包。


以上是文档中的安装说明，接下来聊一下具体的使用逻辑。

---

## 通过服务器运行 p5js 文件
![image](https://github.com/user-attachments/assets/b5e8cbd5-e19b-497e-9aad-4ba256f0f392)

通过服务器运行本地 p5js 文件。

![image](https://github.com/user-attachments/assets/1e321124-b0a6-420b-ab34-0797f4c7947f)

![image](https://github.com/user-attachments/assets/7157fa36-685f-4436-b921-456751ab3655)

以 p5-basic 为例，用 [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) 启动。

`p5-basic -> sketch.js`

``` js
function setup() {
	createCanvas(500, 500);
	setupOsc(12000, 3334);
}

function setupOsc(oscPortIn, oscPortOut) {
	var socket = io.connect('http://127.0.0.1:8081', { port: 8081, rememberTransport: false });
	socket.on('connect', function() {
		socket.emit('config', {
			server: { port: oscPortIn,  host: '127.0.0.1'},
			client: { port: oscPortOut, host: '127.0.0.1'}
		});
	});
	socket.on('message', function(msg) {
		if (msg[0] == '#bundle') {
			for (var i=2; i<msg.length; i++) {
				receiveOsc(msg[i][0], msg[i].splice(1));
			}
		} else {
			receiveOsc(msg[0], msg.splice(1));
		}
	});
}
```

`setupOsc(oscPortIn, oscPortOut)` 函数的两个传参，分别是 **接收端口** 和 **输出端口**。

``` js
function receiveOsc(address, value) {
	console.log("received OSC: " + address + ", " + value);

	if (address == '/test') {
		x = value[0];
		y = value[1];
	}
}

function sendOsc(address, value) {
	socket.emit('message', [address].concat(value));
}
```

`receiveOsc(address, value)` / `sendOsc(address, value)` 分别用于接收 / 发送信号，传参都是 `address` / `value` 两个值，这涉及到 OSC 信号的构成。

OSC 信号通过以下几个部分构成：
- IP 地址 / IP Address
- 端口号 / Port
- 地址路径 / Address Path
- 值 / Value

在 `setup()` 中 `setupOsc(12000, 3334)`，意味着 OSC 的接收端口为 12000，发送端口为 3334；

在 `receiveOsc()` 中可以看到：
``` js
	if (address == '/test') {
		x = value[0];
		y = value[1];
	}
```
表示如果地址路径为 `/test`，就根据 **地址路径** 的 **值** 设置变量。

## 项目测试
![image](https://github.com/user-attachments/assets/3d334fef-acbb-422a-99ec-661bea564ac8)

1. 创建 OSC 发送信号（这里用 [MaxMsp](https://cycling74.com/) 创建，你可以通过任意趁手的 OSC 工具完成）;

 ![image](https://github.com/user-attachments/assets/af19a478-7301-42eb-a49c-08cc62a1e919)

 2. 启动 `bridge.js`;

![image](https://github.com/user-attachments/assets/7157fa36-685f-4436-b921-456751ab3655)

3. 通过服务器启动 `p5-basic` 项目；

`p5-basis -> sketch.js` 中，变量 x、y 用于控制圆的 x、y 位置。OSC 发送地址路径为 `/text` 的两个随机值。

![20241027-000359-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/b764f2bb-82a0-4eb5-ab9b-4c0d514e20d8)

接下来你可以依照这个逻辑，通过自定义变量和 osc 信号控制任意参数，希望你玩的开心，祝顺利。

# 欢迎来到编程世界 - soulhacker
![image](https://github.com/user-attachments/assets/080b50dd-7d28-4b86-a3c6-a3549c3ff2dc)

[欢迎来到编程世界 - soulhacker](https://space.bilibili.com/760331/channel/collectiondetail?sid=353626&spm_id_from=333.788.0.0)，中文世界最好的编程入门课程



# 在线制作字体子集
![image](https://github.com/user-attachments/assets/77224a2f-d1cb-461d-a734-40a1e0994018)

很多时候你只需要字体中的一部分文字，尤其是中文字体，可以极大地减轻文件体积，加快运行速度，[transfonter](https://transfonter.org/) 可以帮你以最轻量的方式完成这件事。

# Max Msp 实现不重复的随机数
![image](https://github.com/user-attachments/assets/6f57af3c-1fbd-4854-a531-11c45a459a40)

[Mas Msp 实现不重复的随机数](https://cycling74.com/forums/randome-no-duplicates#reply-5baf692dc44d2d74edd2697d)

# Max Map 实现不重复的随机数组
![image](https://github.com/user-attachments/assets/14e42608-ca3b-476c-98e6-1950c48f8adc)

[Max Map 实现不重复的随机数组](https://cycling74.com/forums/randome-no-duplicates#reply-58ed21786908cf22c8395973)

# 小白兔白又白
![IMG_7682](https://github.com/user-attachments/assets/045018d5-09db-4ce4-9792-f40955b736e2)

# SOMETHING NEW - 高橋幸宏
![image](https://github.com/user-attachments/assets/620ab640-71e4-4259-8e51-f3fc9d342bcc)
