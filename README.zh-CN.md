# Halcon Go

<p align="center">
  <strong>面向 Visual Studio 2022 + C# + HALCON 的调试变量观察台</strong>
  <br>
  <span>从断点打开真实 HALCON 对象，直接检查图像、区域、Tuple、Dict 和本地变量文件。</span>
</p>

<p align="center">
  <a href="README.zh-CN.md"><strong>中文</strong></a>
  ·
  <a href="README.en.md">English</a>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.8/HalconVariableInspectorSetup-1.0.8.exe"><img alt="下载 v1.0.8" src="https://img.shields.io/badge/下载-v1.0.8-21b8a6?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json"><img alt="更新通道" src="https://img.shields.io/badge/更新通道-stable-0f172a?style=for-the-badge"></a>
  <img alt=".NET Framework" src="https://img.shields.io/badge/.NET_Framework-4.7.2+-5b8def?style=for-the-badge">
  <img alt="Visual Studio" src="https://img.shields.io/badge/Visual_Studio-2022-7c5cff?style=for-the-badge">
</p>

## 立即下载

| 项目 | 内容 |
| --- | --- |
| 当前版本 | 1.0.8 |
| 更新日期 | 2026-06-11 |
| 安装包 | [HalconVariableInspectorSetup-1.0.8.exe](https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.8/HalconVariableInspectorSetup-1.0.8.exe) |
| 文件大小 | 2.4 MB |

## 功能亮点

| 能力 | 说明 |
| --- | --- |
| VS 调试器放大镜 | 从 C# 断点直接打开 HALCON 变量，不需要临时导出。 |
| 独立文件查看 | 支持拖拽图片、文件夹、`.hobj`、`.tup`、`.hdict`。 |
| 区域可视化 | 固定 LUT12 颜色序列，支持 Region 和 XLD 叠加。 |
| 图像分析 | 通道切换、像素读数、阈值预览、灰度剖面和直方图。 |
| 测量与标注 | 支持距离、Dx、Dy、角度、ROI 框、圆形 ROI 和手绘标注。 |
| 截图复制 | 图像窗口截图以 PNG 直接写入剪贴板。 |
| 大对象保护 | 按需加载和安全预览降低 UI 卡顿风险。 |
| 在线更新 | 读取公开更新清单，完成完整性校验后启动安装器。 |

## 安装

1. 下载上方安装包。
2. 关闭 Visual Studio、正在调试的程序和已打开的查看器窗口。
3. 运行安装器，建议使用默认 Visual Studio 2022 Visualizers 目录。
4. 安装完成后重启 Visual Studio。

默认安装位置：

```text
C:\Users\<User>\Documents\Visual Studio 2022\Visualizers
```

## 环境要求

| 项目 | 要求 |
| --- | --- |
| 系统 | Windows x64 |
| IDE | Visual Studio 2022 |
| 运行框架 | .NET Framework 4.7.2 或更高版本 |
| 普通图像 | 图片文件不依赖 HALCON Runtime |
| VS 变量和 HALCON 原生文件 | 读取 `.hobj`、`.tup`、`.hdict` 或调试变量时，需要目标电脑具备 HALCON Runtime、HALCON .NET DLL 和合法授权 |

## 更新校验

Viewer 会读取公开更新清单：

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

当有新版本时，工具内更新按钮会下载安装包并完成完整性校验；通过后才会启动安装器。

## 分发范围

本页只提供安装包、更新清单和使用说明。安装包不包含 HALCON Runtime、HALCON 配置或授权文件，目标电脑需要自行准备对应环境。
