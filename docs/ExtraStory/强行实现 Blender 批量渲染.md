# 强行实现 Blender 批量渲染

Blender 操作界面中并没有批量渲染的选项，但「批量渲染」这个需求还是有的，守在电脑前一个一个点渲染按钮这种近乎癫狂的举动显然是不可取的，所以需要更自动化的办法来实现这个需求。

![image](https://user-images.githubusercontent.com/20842136/159113993-b9b298db-1509-4d87-80a1-4138f2b6903f.png)

整体逻辑就是通过命令的方式，在后台启动 Blender 渲染文件，面对批量渲染需求时，​让多条命令依次执行。

<!-- 
# 编程环境配置
![image](https://user-images.githubusercontent.com/20842136/158941387-865e78cd-2d09-4339-9327-675013eb52a0.png)

我们要用到的命令需要一个执行环境，所以首先要进行基础的环境配置。

关于基础环境配置，这篇 [《编程环境配置指南》](https://github.com/neolee/pilot/blob/master/x1-setup.md) 就足够了，还不用看完，这篇指南最后会讲到 Python 的安装，你不需要看到这一步，只要安装好与操作系统相对应的软件包管理工具（win-Scoop / Mac-Homebrew）即可。

这一步你已经安装好 ConEmu 和 Scoop（win）或 Homebre（Mac）。 -->

# 准备命令行工具
命令需要在执行环境中运行，也就是命令行工具，这也是实现批量渲染的第一步。

## Windows
Window 用户建议安装 [ConEmu](https://conemu.github.io/)（[配置指南](https://github.com/neolee/pilot/blob/master/x1-setup.md)）。
![image](https://user-images.githubusercontent.com/20842136/158942878-0de6b2a0-1ff7-468a-884e-6e46444503b6.png)
*ConEmu*

## MacOS
Mac 用户使用系统自带的「终端」或安装 [iTerm2](https://iterm2.com/)。
![image](https://user-images.githubusercontent.com/20842136/158942899-50c3af8e-ca15-4d3a-b491-56f6c9eed8ea.png)
*iTerm2*

# 通过命令行启动 Blender
## Window
![Snipaste_2022-03-19_16-58-18](https://user-images.githubusercontent.com/20842136/159114707-eb8bf7ef-1693-4a52-b73d-418af9130c45.png)

Windows 用户可以进入 Blender 安装目录，文件夹空白处点击右键，通过「ConEmu」打开。

![Snipaste_2022-03-19_16-59-55](https://user-images.githubusercontent.com/20842136/159114806-565042d3-3cac-4006-a6e6-b88f1c6f4cba.png)

此时命令行工具是这个状态，代表你所处的位置在 Blender 安装目录下。

## MacOS
![image](https://user-images.githubusercontent.com/20842136/159115043-16050ef9-71c3-4d5e-9e3f-6da9c45c9f8e.png)

Mac 用户啥也不用干，打开「终端」或「iTerm2」就好。

此时你可以尝试在命令行中输入 `blender`，会发现 Blender 通过命令被启动了。平常我们通过点击图标启动，本质上也是电脑在后台执行了一系列命令，点击图标是更方便快捷的办法，每个图标一定有与之相对的命令（功能），但是命令却不一定有相对应的图标，比如批量渲染，所以它需要通过命令的方式完成。

# Blender 命令
![image](https://user-images.githubusercontent.com/20842136/159115144-965911ce-1076-436b-9441-8d9ba04c1503.png)

Blender 开放了很多功能（参考 [命令行参数](https://docs.blender.org/manual/zh-hans/latest/advanced/command_line/arguments.html)），当前我们只需要了解关于渲染的部分。

Blender 命令行用法：`blender [参数][文件][参数]`。

```
-b
在后台运行渲染(通常用于无需UI的渲染)。
```
```
-a
渲染从开始到结束帧(包含最后帧)。
```
```
-f
渲染某一帧并保存。
```
**例：**
```
blender -b RenderTest.blend -a
渲染 RenderTest.blend 从开始帧到结束帧，并保存。
```
```
blender -b RenderTest.blend -f 1
渲染 RenderTest.blend 第一帧，并保存。
```

# 通过命令行渲染
![Snipaste_2022-03-19_17-44-21](https://user-images.githubusercontent.com/20842136/159116156-55324140-ec98-4aa0-9ecc-24d5299cf730.png)
首先在准备渲染的 Blender 文件中，设置文件输出位置/格式。

![image](https://user-images.githubusercontent.com/20842136/159115925-e3dac91e-ad25-4911-b33d-f4a85566fad0.png)
找到该文件右键（Win shift+右键 / Mac option+右键）复制文件路径。

![Snipaste_2022-03-19_17-39-21](https://user-images.githubusercontent.com/20842136/159115998-dca5f0d1-ae3f-49f7-991b-6b1dbd6e45fc.png)
回到命令行，输入 `blender -b [粘贴刚刚复制的文件路径] -a`，还记得上面的举例吗，`-a` 代表渲染全部帧；`-f x` 代表渲染某一帧，按需选择，接着点击回车运行命令，就能看到渲染进程啦。

![ezgif com-gif-maker](https://user-images.githubusercontent.com/20842136/159116273-db983ffd-2f87-449b-b5bf-f7ac7f5975be.gif)

# 批量渲染
![image](https://user-images.githubusercontent.com/20842136/159116894-44af4fa6-db84-4624-9d19-04df1aea24bc.png)

现在你已经掌握通过命令行执行一条渲染命令，当前的核心需求「批量渲染」就是执行多条命令，这比前面的步骤简单很多。

![Snipaste_2022-03-19_18-11-17](https://user-images.githubusercontent.com/20842136/159116977-7592a126-b2ef-4077-922e-f9909cc19e59.png)

比如有 `01.blend`/`02.blend` 两个需要渲染的文件，它们的渲染命令分别是 `blender -b 01.blend -a` 和 `blender -b 02.blend -a`，把两条命令连在一块执行肯定是不行的，你也别管我是怎么知道的。

当需要批量渲染时，只需要在两条命令中间加入 `&`（逻辑运算符「与」）即可：`blender -b 01.blend -a & blender -b 02.blend -a` ，这条命令指的是执行 01.blend 与 02.blend 两条渲染命令，如果你还有 03、04、05 渲染文件，那就用 `&` 连接每一条渲染命令，接着让电脑自己干活就好，你去玩吧。

# 最后
上文提到需要在 Blender 软件中设置文件输出位置/格式，其实这些也可以通过命令完成，这篇文章主要聚焦批量渲染的问题，所以简化了渲染之外的其它命令，更多命令请参考 [官方命令行参数文档](https://docs.blender.org/manual/zh-hans/latest/advanced/command_line/arguments.html)。

祝你顺利，下期再见。