# 很大声周刊-vol.157 | Oh My Posh 安装 / 配置

[Oh My Posh](https://ohmyposh.dev/) 可以让你的终端好看一点，就像 maxOC 那边的 [Oh My Zsh](https://ohmyz.sh/)。

![Image](https://github.com/user-attachments/assets/b45bba67-d237-4dfa-9bc5-7dcd56e0eac5)

Windows 默认终端 (Windows Terminal）是跟随系统更新的，建议使用独立版本的 [PowerShell](https://github.com/PowerShell/PowerShell)，以下会用 PowerShell 7 演示（默认终端也可以）。

跟随 [Oh My Posh 文档：](https://ohmyposh.dev/docs/installation/windows)

## 安装

```
winget install JanDeDobbeleer.OhMyPosh -s winget
```

![img](https://github.com/user-attachments/assets/95aa858d-1324-4b5c-8273-915c6800e098)

安装后关闭 PowerShell，重新以管理员身份运行。

## 安装字体
```
oh-my-posh font install
```
![img](https://github.com/user-attachments/assets/721cf7f2-e3e5-4c81-a529-68eb0142be7d)

![img](https://github.com/user-attachments/assets/e7634d02-0065-43d2-9a98-03ef1db914fc)

### Nerd Fonts 字体
![Image](https://github.com/user-attachments/assets/86293b8e-0d5c-48d8-8225-6ef017e0c906)
[Nerd Fonts](https://www.nerdfonts.com/#home) 为开发者提供的字体集合。

可以跳过上方的安装字体步骤，从这里选择、安装字体。

## 配置 Oh My Posh
运行 `echo $PROFILE` 查看配置文件路径，在目标路径中新建 `Microsoft.PowerShell_profile.ps1` 文件。

![img](https://github.com/user-attachments/assets/97cc32c4-f880-4a4e-b24e-13826a689e7e)

用记事本打开这个文件，写入：
```
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/atomic.omp.json" | Invoke-Expression
```

使用 atomic.omp.json 初始化 Oh My Posh，其中 `atomic` 是 Oh My Posh 提供的主题名称，你可以在 [主题列表](https://ohmyposh.dev/docs/themes) 中挑选自己喜欢的主题替换。

![img](https://github.com/user-attachments/assets/ea8fa5b1-49d4-4a58-b3ac-99bd6330ff09)

接下来重启 PowerShell，这时界面中有乱码，因为还没设置字体，点击顶栏下三角箭头，打开设置页面，选择刚刚安装好的字体即可。

![img](https://github.com/user-attachments/assets/098a76e7-8586-4d1c-b5cb-fa421a75ffb8)

![img](https://github.com/user-attachments/assets/bf67dda0-7062-480d-9ab9-5b15345b05c2)

过程严重抄袭[《windows中使用Oh My Posh美化你的终端PowerShell或CMD》](https://cloud.tencent.com/developer/article/2442201)，并做了一定简化。








