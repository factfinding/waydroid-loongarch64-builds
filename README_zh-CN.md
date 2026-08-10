# LoongArch64 Waydroid 镜像

简体中文 | [English](README.md)

用于在 LoongArch64 Linux 主机上运行 Waydroid 的实验性 LineageOS 23.2 /
Android 16 镜像。

本仓库用于发布经过测试的二进制版本。请前往
[Releases](https://github.com/factfinding/waydroid-loongarch64-builds/releases)
页面下载文件，并查看各版本对应的安装说明、校验和及已知问题。

## 当前状态

- Waydroid 可以启动并进入可交互的 Android 桌面。
- 当前镜像使用 Android 16 BP4A 发布配置；Launcher3 和最近任务界面已在
  LoongArch64 测试设备上验证。
- 支持 LoongArch64 Android 应用。
- Chromium WebView 和宿主音频可以使用。
- 可通过实验性的 Native Bridge 运行 ARM64 应用，但兼容性仍不完整。
- 图形加速可以使用，但转译应用和游戏可能运行较慢或遇到兼容性问题。

## 宿主环境要求

当前版本面向以下环境：

- LoongArch64 架构的 AOSC OS；
- 支持 binder/binderfs 的 4 KiB 或 16 KiB 页面大小内核；
- Wayland 桌面会话；
- Release 中提供的修订版 Waydroid 和 LXC 软件包。

开发期间使用的 AOSC LXC 原始软件包在 LoongArch64 上禁用了 seccomp。除非该打包
差异已经在上游修复，否则不能用源中的原始软件包替代 Release 提供的版本。

## 安装

请从同一个 Release 下载所有必要文件，并严格按照该版本的 Release 说明进行安装。
一个完整版本预计包含：

- `system.img.zst`；
- `vendor.img.zst`；
- 修订后的 Waydroid 宿主软件包；
- 启用了 seccomp 的 AOSC LXC 软件包；
- `SHA256SUMS`。

请勿混用不同 Release 的 Android 镜像或宿主软件包。替换镜像前，请备份现有的
Waydroid 安装。

## 项目范围

这些镜像仅用于测试和开发，不是 Waydroid、LineageOS、AOSP、AOSC 或龙芯的官方
发行版本。

## 许可证

本仓库中的材料采用 GPL-3.0 许可证，详见 [LICENSE](LICENSE)。Release 中的二进制
文件包含多个上游项目，各组件仍遵循各自的许可证。
