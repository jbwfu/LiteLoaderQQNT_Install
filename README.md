# LiteLoaderQQNT_Install
针对 [LiteLoaderQQNT](https://liteloaderqqnt.github.io) 的安装脚本

同时安装 ltxhhz 大佬编写的[插件列表查看](https://github.com/ltxhhz/LL-plugin-list-viewer/)

**最推荐的插件安装方式目前仍是手动安装**

**若出现 LiteLoaderQQNT 成功安装，而设置中没有 LiteLoaderQQNT 选项时极有可能是存在插件问题，一般均由用户在插件商店选择的错误安装方式导致**

## 最新版本支持

[![Windows](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/windows.yml/badge.svg)](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/windows.yml)
[![Linux](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/linux.yml/badge.svg)](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/linux.yml)
[![macOS](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/macOS.yml/badge.svg)](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/macOS.yml)
[![AppImage](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/appimage.yml/badge.svg)](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/appimage.yml)


## 使用方法

### Windows

运行对应 exe 即可：[Releases 下载链接](https://github.com/Mzdyl/LiteLoaderQQNT_Install/releases/latest/download/install_windows.exe)
或从 [Github Action](https://github.com/Mzdyl/LiteLoaderQQNT_Install/actions/workflows/windows.yml) 获取测试版

### Linux/macOS

下载运行 [Releases](https://github.com/Mzdyl/LiteLoaderQQNT_Install/releases/latest) 中对应脚本或者终端输入下方指令运行

```shell
bash <(curl -s -L "https://github.com/Mzdyl/LiteLoaderQQNT_Install/raw/main/install.sh")
```

更多自定义支持见 `install.sh --help`

## 版本支持

理论支持 QQNT 桌面端 全架构 全版本(NT 旧版本会存在显示错误，推荐使用较新版本)
据反馈,在 Windows 8 之前版本版本无法正常运行安装程序(action 中采用的是 Python3.9 打包, py3.9 不支持 win8 之前版本系统)

## 升级更新

更新 LiteLoaderQQNT 版本一样可以使用 脚本/exe 进行保留数据升级

## 针对仓库内其他文件的附加说明

install_mac_launchd.sh 是给 macOS 写的设定环境变量的版本

但是由于 macOS 严格的软件沙盒限制，会遇到大量权限问题，**无法正常使用**，仅作为后续研究用

普通用户还请使用 install.sh

## 常见问题

**Windows 用户请确保使用 管理员身份运行。**

**macOS 遇到 Operation not permitted 请检查是否给予 终端 完全磁盘访问权限 或者 允许 终端想访问其他App的数据 以及 App管理 中允许 终端。**

**LiteLoaderQQNT 安装后无法使用插件请自行检测原因或加群交流，本脚本仅负责安装，同时步骤完全遵循官网指南**

**如有[报毒](https://github.com/Mzdyl/LiteLoaderQQNT_Install/issues/20)请自行判断，本代码完全开源，同时发布的 exe 均由 GitHub Actions 通过 pyinstaller 及 Nuitka 构建，代码公开可以自行审查**

软件目前使用 GitHub Action 自动化验证脚本效果

如仍有其他问题或者 bug 欢迎友好反馈

**安装器反馈群 :  [Telegram](https://t.me/+EKoVlfEI7Ow4MzJl)**

LiteLoaderQQNT群: [Telegram](https://t.me/LiteLoaderQQNT)

## TODO List

- [x] [repack_appimage.sh](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/repack_appimage.sh) 添加选择QQ.AppImage路径功能
- [x] [install_linux.sh](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_linux.sh) 更通用环境变量设置以及特殊shell的适配
- [x] [install_linux.sh](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_linux.sh) 添加 Arch Linux 下提示可以使用 aur liteloaderqqnt-bin
- [x] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py) 避免权限问题，如WinError5
- [x] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py) 更新打包方式，替代PyInstaller，避免报毒
- [x] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py)  357a79e 提交导致 Nuitka 构建失败？
- [x] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py)  考虑打包 LiteloaderQQNT 文件进安装器，实现离线更新？
- [x] [install.sh](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install.sh) 使用 release 版本而不是直接 git 拉取源码
- [x] [.github/workflows ](https://github.com/Mzdyl/LiteLoaderQQNT_Install/tree/main/.github/workflows) 更新QQ安装包版本
- [x] [README.md](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/README.md) 使用GitHub徽章显示通过自动化 ci 监测 LL 与 QQ 最新版的兼容状态
- [x] [install_mac.sh](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_mac.sh) **研究如何快速复制 plugins 和 data 文件夹（NEED HELP）**
- [x] [install.sh](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install.sh) 跟上 win 代码的反代逻辑，目前的过于简陋
- [ ] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py) 已经发现的潜在问题修复
- [ ] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py) 精简代码，现在太屎山了
- [ ] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py) 完善下版本判断，小于10MB太抽象了
- [ ] [install_windows.py](https://github.com/Mzdyl/LiteLoaderQQNT_Install/blob/main/install_windows.py) 是否需要其他插件安装功能？

## 特别鸣谢：

[LiteLoaderQQNT](https://github.com/LiteLoaderQQNT/LiteLoaderQQNT)

windows脚本借用 [QQNTFileVerifyPatch](https://github.com/LiteLoaderQQNT/QQNTFileVerifyPatch) 项目代码实现修补

附加安装的[插件列表查看](https://github.com/ltxhhz/LL-plugin-list-viewer/)
