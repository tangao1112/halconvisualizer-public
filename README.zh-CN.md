# HALCON 变量查看器

<p align="center">
  <strong>在 C# 断点处直接查看 HALCON 图像、区域、Tuple 和 Dict。</strong>
</p>

<p align="center">
  <a href="README.md">English</a>
  ·
  <a href="README.zh-CN.md">中文</a>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><img alt="下载最新版" src="https://img.shields.io/badge/下载-v1.0.3-21b8a6?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json"><img alt="更新通道" src="https://img.shields.io/badge/更新-stable-21b8a6?style=for-the-badge"></a>
  <img alt=".NET Framework" src="https://img.shields.io/badge/.NET_Framework-4.7.2+-5b8def?style=for-the-badge">
  <img alt="Visual Studio" src="https://img.shields.io/badge/Visual_Studio-2022-7c5cff?style=for-the-badge">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-x64-222b36?style=for-the-badge">
</p>

<p align="center">
  <a href="#下载">下载</a>
  ·
  <a href="#功能">功能</a>
  ·
  <a href="#环境要求">环境要求</a>
  ·
  <a href="#更新机制">更新机制</a>
</p>

```text
C# 断点
    -> Visual Studio 放大镜
        -> HALCON 图像 / 区域 / Dict / Tuple 查看器
            -> 查看、测量、复制截图、继续调试
```

## 下载

安装最新公开版本：

<p>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><strong>下载 HalconVariableInspectorSetup-1.0.3.exe</strong></a>
</p>

公开更新清单：

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

安装器会把 Visual Studio 调试可视化插件和独立 Viewer 安装到当前用户的 Visual Studio 2022 Visualizers 目录。

## 功能

- 从 Visual Studio Watch、Locals、Autos 直接打开 `HObject`、`HImage`、`HRegion`、`HXLDCont`、`HTuple`、`HDict`。
- 查看图像、区域和 XLD 叠加，区域使用固定 LUT 风格颜色。
- 将 `.hobj`、`.tup`、`.hdict`、`.hvx`、图片或文件夹拖入独立 Viewer。
- 查看灰度剖面、直方图、像素值、测量结果和图像通道。
- 将图像窗口截图以 PNG 形式直接复制到剪贴板。
- 通过按需加载和大对象安全预览，降低 Visual Studio 卡顿风险。

## 为什么做这个工具

HALCON 在 HDevelop 内的工具很强，但 C# 调试需要更快地从断点切到真实 HALCON 数据。

这个工具聚焦一个短调试链路：

```text
断点暂停 -> 打开变量 -> 检查对象 -> 继续调试
```

它适合需要频繁核对真实中间变量的算法工程师，减少手动导出对象和切换工具的时间。

## 亮点

| 场景 | 能力 |
|---|---|
| Visual Studio 调试 | 通过调试器放大镜打开 HALCON 变量 |
| 独立查看 | 拖拽文件和文件夹到 Viewer |
| 图像检查 | 通道切换、像素读数、缩放、平移、适应窗口 |
| 区域叠加 | 固定 LUT 风格颜色，支持填充和轮廓模式 |
| 分析工具 | 距离测量、灰度剖面、直方图 |
| 工作流 | 直接复制 PNG 截图到剪贴板 |
| 大数据 | 按需加载和安全预览减少界面阻塞 |

## 环境要求

- Windows。
- Visual Studio 2022。
- .NET Framework 4.7.2 或更高版本。
- 读取 `.hobj`、`.tup`、`.hdict` 等 HALCON 原生文件时，需要目标电脑具备 HALCON Runtime 和合法 HALCON 授权。

普通图片文件和 `.hvx` 快照不依赖 HALCON Runtime。

## 更新机制

Viewer 会读取：

```text
update/latest.json
```

当发布新版本时，工具内的更新按钮会下载安装包、校验 SHA256，然后启动安装器。

公开发布目录结构：

```text
update/latest.json
downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe
```

## 仓库范围

这个公开仓库只作为二进制分发和更新通道，包含：

- 公开更新清单。
- 公开安装包。

这里不包含私有源码。

## 说明

安装包不包含 HALCON Runtime、HALCON 配置或授权文件。目标电脑如果需要读取 HALCON 原生文件，需要自行配置 HALCON 环境。
