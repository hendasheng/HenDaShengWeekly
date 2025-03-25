# 很大声周刊-vol.156 | TangoFlux （文本到音频生成模型） - 本地安装

![Image](https://github.com/user-attachments/assets/fc1381ee-4db3-46c8-b889-762039d2f299)
[TangoFlux](https://github.com/declare-lab/TangoFlux) 是由 DeCLaRe 实验室和 NVIDIA 合作推出的文本到音频生成模型（[在线体验](https://huggingface.co/spaces/declare-lab/TangoFlux)）。

如果你从事声音、影像类工作，TangoFlux 会带来很大的帮助。

文档中的方法简单且硬核，在缺少前置条件的情况下很容易出错，折腾好久才安装成功，我猜不止有我在过程中遇到问题，所以记录一下完整的安装过程。

这不是二次加工过的的“一键安装”版本，而是最质朴的安装方式，通过它可以更多了解工具的底层逻辑和依赖关系，我想这个过程对接下来探索整个开源世界都有一定帮助。

[TangoFlux 文档](https://github.com/declare-lab/TangoFlux) 中从这里开始：
```
pip install git+https://github.com/declare-lab/TangoFlux
```
在此之前需要一些前置准备，确保你安装了：
- Python、pip 和 Git，并且对它们稍有了解；
- NVIDIA 驱动 / CUDA Toolkit；

![Image](https://github.com/user-attachments/assets/b53960b1-ce67-4563-bb35-d98094b91ae1)

## 创建 Python 虚拟环境

接下来开始安装，第一步需要创建 python 虚拟环境，安装命令会自动安装很多依赖项，创建虚拟环境是为了确保没有版本冲突，在这个环境中只有 TangeFlux 和它的依赖项。

``` Js
// 创建虚拟环境 / TangoFlux 是这个虚拟环境的命名
python -m venv TangoFlux

// 激活虚拟环境
cd TangeFlue
cd Script
activate
```

![Image](https://github.com/user-attachments/assets/143597d2-b562-47e0-a4b1-a0fb26023480)

## 安装 TangeFlux

接着开始文档中的步骤：
``` js
// 自动安装 TangoFlux 依赖项
pip install git+https://github.com/declare-lab/TangoFlux
```

``` js
// 运行 TangeoFlux
tangoflux-demo
```

到这里就算完成了，但是大概率会遇到 `找不到指定模块 ... fbgemm.dll` 报错。
![Image](https://github.com/user-attachments/assets/ed730396-66de-42bd-8abe-dccbe7335a36)

这里参考这篇文章 [《解决“OSError: [WinError 126] 找不到指定的模块”》](https://www.bilibili.com/opus/967745334024339490)

## 下载 dll 文件依赖分析工具 Dependencies

[Dependencies](https://github.com/lucasg/Dependencies
) 帮助 Windows 开发人员解决他们的 dll 加载依赖关系问题。

![Image](https://github.com/user-attachments/assets/35e2e45e-6b04-49ef-8a39-21996be17dc3)

根据系统下载对应版本，解压后运行 `DependenciesGui.exe`，File -> Open 打开报错信息路径中的 fbgemm.ddl 文件。

![Image](https://github.com/user-attachments/assets/68074e0f-2b15-4f08-a877-16be75bf05cf)

标红表示缺少文件，打开 [DDLme](https://www.dllme.com/dll/files/libomp140_x86_64/versions)，下载对应版本。

![Image](https://github.com/user-attachments/assets/597a85f4-48f0-488d-8f80-e3954526268f)

将文件中的 `libomp140.x86_64.dll` 文件复制到报错文件夹中。

重新运行 `tangoflux-demo` 就完成啦。

![Image](https://github.com/user-attachments/assets/9f01f76f-b00f-4bd4-8028-fbce37f32d49)

## 为什么生成速度超级慢
![Image](https://github.com/user-attachments/assets/2456a2f8-15f2-41b6-a3bc-041bb961a5b8)

![Image](https://github.com/user-attachments/assets/ec9c1c18-87d2-49ff-a2ec-6f636e09ece1)

当你尝试生成音频时会发现速度超级慢，原因在于它并没有调用 GPU（命令行中 `nvidia-smi` 可以查看 GPU 状态）。

这里大家的各种工具版本不同，可以借助任意 AI 工具给出相应的解决方案，我在这里用到 Grok。

![Image](https://github.com/user-attachments/assets/a70775b1-e274-451a-a675-702b93a2806b)

核心问题在于当前虚拟环境中安装的 PyTorch 是 CPU 版本，不支持 GPU。

```js
// 这里是示意，你需要根据你的环境选择相应的版本

// 先卸载掉当前 CPU 版 PyTorch
pip uninstall torch torchvision torchaudio

// 安装支持 CUDA 12.7 的 PyTorch
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

```

到这里就全部解决了，再次运行 `tangoflux-demo` 会发现速度有了明显的提升。

以上是 TanglFlux 安装、排查、解决问题的全过程，你也可以参考以上步骤和方法完成本地安装，祝顺利 🍻。













