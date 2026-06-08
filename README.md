# HALCON 变量查看器

<p align="center">
  <strong>面向 Visual Studio 2022 + C# + HALCON 的调试变量观察台</strong>
  <br>
  <span>从断点打开真实 HALCON 对象，直接检查图像、区域、Tuple、Dict 和本地变量文件。</span>
</p>

<p align="center">
  <a href="README.md"><strong>中文</strong></a>
  ·
  <a href="README.en.md">English</a>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><img alt="下载 v1.0.3" src="https://img.shields.io/badge/Download-v1.0.3-21b8a6?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json"><img alt="更新通道" src="https://img.shields.io/badge/Update-stable-0f172a?style=for-the-badge"></a>
  <img alt=".NET Framework" src="https://img.shields.io/badge/.NET_Framework-4.7.2+-5b8def?style=for-the-badge">
  <img alt="Visual Studio" src="https://img.shields.io/badge/Visual_Studio-2022-7c5cff?style=for-the-badge">
</p>

```text
C# Breakpoint
    -> Visual Studio Magnifier
        -> HALCON Variable Inspector
            -> Image / Region / Tuple / Dict / Local Files
                -> Inspect / Measure / Copy Snapshot / Continue Debugging
```

## 立即下载

<p>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><strong>下载 HalconVariableInspectorSetup-1.0.3.exe</strong></a>
</p>

安装器会把 Visual Studio 调试可视化插件、独立 Viewer、卸载程序和更新能力安装到当前用户的 Visual Studio 2022 Visualizers 目录。

```text
C:\Users\<User>\Documents\Visual Studio 2022\Visualizers
```

## 调试闭环

| 阶段 | 工程师看到什么 | 工具做什么 |
|---|---|---|
| 断点暂停 | Watch、Locals、Autos 里的 HALCON 变量 | 通过放大镜打开真实变量 |
| 变量展开 | `HObject`、`HImage`、`HRegion`、`HTuple`、`HDict` | 生成可视化快照并启动 Viewer |
| 图像检查 | 通道、像素值、缩放、平移、适应窗口 | 保持交互响应，避免阻塞 VS |
| 区域叠加 | 固定 LUT 风格颜色、填充、轮廓 | 按稳定顺序显示对象区域 |
| 结果复核 | 灰度剖面、直方图、测量、截图复制 | 把调试证据直接放进剪贴板 |

## 能力矩阵

| 能力 | 说明 |
|---|---|
| VS 调试器放大镜 | 从 C# 断点直接打开 HALCON 变量，不需要临时导出代码 |
| 独立文件查看 | 支持拖拽 `.hobj`、`.tup`、`.hdict`、`.hvx`、图片和文件夹 |
| 区域可视化 | 固定 LUT 式颜色序列，支持 Region 和 XLD 叠加 |
| 图像分析 | 单通道、多通道、像素读数、灰度剖面、直方图 |
| 工作流输出 | 图像窗口截图以 PNG 直接复制到剪贴板 |
| 大对象保护 | 按需加载和安全预览降低卡顿风险 |
| 更新通道 | 读取公开清单，校验 SHA256 后启动安装器 |

## 为什么它重要

HALCON 在 HDevelop 里很强，但 C# 调试常常卡在一个问题上：真实中间变量在断点处，视觉判断却在另一个工具里。

这个 Viewer 解决的是短路径：

```text
暂停 -> 打开变量 -> 看图和区域 -> 判断算法状态 -> 继续调试
```

它面向算法工程师，不是通用相册工具。重点是准确读取 HALCON 变量、稳定显示区域、快速切换通道，并且不把 Visual Studio 拖进长时间未响应。

## 环境要求

| 项目 | 要求 |
|---|---|
| 系统 | Windows x64 |
| IDE | Visual Studio 2022 |
| 运行框架 | .NET Framework 4.7.2 或更高版本 |
| HALCON 原生文件 | 读取 `.hobj`、`.tup`、`.hdict` 时，目标电脑需要 HALCON Runtime 和合法授权 |
| 普通图像和快照 | 图片文件与 `.hvx` 快照不依赖 HALCON Runtime |

## 更新机制

Viewer 会读取公开版本清单：

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

发布目录结构：

```text
update/latest.json
downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe
```

当有新版本时，工具内更新按钮会下载安装包、校验 SHA256，然后启动安装器。公开仓库只提供二进制安装包和更新清单。

## 仓库范围

这个仓库是公开分发通道，包含：

| 内容 | 是否包含 |
|---|---|
| 安装包 | 是 |
| 更新清单 | 是 |
| 私有源码 | 否 |
| HALCON Runtime | 否 |
| HALCON 授权文件 | 否 |

目标电脑需要自行准备 HALCON Runtime、HALCON 配置和授权。安装器不会修改目标电脑的 HALCON 配置。
