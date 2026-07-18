# Halcon Go

<p align="center">
  <strong>A Visual Studio 2022 + C# + HALCON variable inspection cockpit.</strong>
  <br>
  <span>Open real HALCON runtime objects from a breakpoint, then inspect images, regions, tuples, dictionaries, and local variable files.</span>
</p>

<p align="center">
  <a href="README.zh-CN.md">中文</a>
  ·
  <a href="README.en.md"><strong>English</strong></a>
</p>

<p align="center">
  <a href="https://github.com/tangao1112/halconvisualizer-public/releases/download/v1.1.4/HalconVariableInspectorSetup-1.1.4.exe"><img alt="Download v1.1.4" src="https://img.shields.io/badge/Download-v1.1.4-21b8a6?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json"><img alt="Update channel" src="https://img.shields.io/badge/Update-stable-0f172a?style=for-the-badge"></a>
  <img alt=".NET Framework" src="https://img.shields.io/badge/.NET_Framework-4.7.2+-5b8def?style=for-the-badge">
  <img alt="Visual Studio" src="https://img.shields.io/badge/Visual_Studio-2022-7c5cff?style=for-the-badge">
</p>

## Download

| Item | Value |
| --- | --- |
| Current version | 1.1.4 |
| Updated | 2026-07-18 |
| Installer | [HalconVariableInspectorSetup-1.1.4.exe](https://github.com/tangao1112/halconvisualizer-public/releases/download/v1.1.4/HalconVariableInspectorSetup-1.1.4.exe) |
| Size | 2.9 MB |

## Highlights

| Capability | Description |
| --- | --- |
| Visual Studio debugger magnifier | Open HALCON variables directly from a C# breakpoint. |
| Standalone file viewer | Drag images, folders, `.hobj`, `.tup`, and `.hdict` files into Viewer. |
| Region visualization | Fixed LUT12 color order with Region and XLD overlays. |
| Image analysis | Channel switching, pixel readout, threshold preview, grayscale profile, and histogram. |
| Measurement and annotation | Distance, Dx, Dy, angle, rectangle ROI, circle ROI, and freehand annotation. |
| Screenshot copy | Copy the image-window screenshot directly to the clipboard as PNG. |
| Large-object protection | Lazy loading and safe previews reduce UI stalls. |
| Online update | Reads the public update manifest and verifies package integrity before launching the installer. |

## Installation

1. Download the installer above.
2. Close Visual Studio, the debuggee process, and any open Viewer windows.
3. Run the installer. The default Visual Studio 2022 Visualizers directory is recommended.
4. Restart Visual Studio after installation.

Default install location:

```text
C:\Users\<User>\Documents\Visual Studio 2022\Visualizers
```

## Requirements

| Item | Requirement |
| --- | --- |
| OS | Windows x64 |
| IDE | Visual Studio 2022 |
| Runtime | .NET Framework 4.7.2 or later |
| Plain images | Image files do not require HALCON Runtime |
| Visual Studio variables and native HALCON files | Reading `.hobj`, `.tup`, `.hdict`, or debug variables requires HALCON Runtime, HALCON .NET DLLs, and a valid HALCON license on the target machine |

## Update Verification

Viewer reads the public update manifest:

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

When a newer version is available, the in-app update button downloads the installer and verifies package integrity before launching the installer.

## Distribution Scope

This page provides the installer, update manifest, and usage notes only. The installer does not include HALCON Runtime, HALCON configuration, or HALCON license files; target machines must provide those separately.
