# HALCON Variable Inspector

<p align="center">
  <strong>Inspect HALCON images, regions, tuples, and dictionaries directly from a C# breakpoint.</strong>
</p>

<p align="center">
  <a href="README.md">English</a>
  ·
  <a href="README.zh-CN.md">中文</a>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><img alt="Download latest" src="https://img.shields.io/badge/download-v1.0.3-21b8a6?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json"><img alt="Update channel" src="https://img.shields.io/badge/update-stable-21b8a6?style=for-the-badge"></a>
  <img alt=".NET Framework" src="https://img.shields.io/badge/.NET_Framework-4.7.2+-5b8def?style=for-the-badge">
  <img alt="Visual Studio" src="https://img.shields.io/badge/Visual_Studio-2022-7c5cff?style=for-the-badge">
  <img alt="Windows" src="https://img.shields.io/badge/Windows-x64-222b36?style=for-the-badge">
</p>

<p align="center">
  <a href="#download">Download</a>
  ·
  <a href="#features">Features</a>
  ·
  <a href="#requirements">Requirements</a>
  ·
  <a href="#updates">Updates</a>
</p>

```text
C# breakpoint
    -> Visual Studio magnifier
        -> HALCON image / region / dict / tuple viewer
            -> inspect, measure, copy screenshot, continue debugging
```

## Download

Install the latest public build:

<p>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><strong>Download HalconVariableInspectorSetup-1.0.3.exe</strong></a>
</p>

Public update manifest:

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

The installer places the Visual Studio debugger visualizer and standalone viewer into the current user's Visual Studio 2022 Visualizers directory.

## Features

- Open `HObject`, `HImage`, `HRegion`, `HXLDCont`, `HTuple`, and `HDict` from Visual Studio Watch, Locals, or Autos.
- View images, regions, and XLD overlays with fixed LUT-style region colors.
- Drag `.hobj`, `.tup`, `.hdict`, `.hvx`, images, or folders into the standalone viewer.
- Inspect grayscale profiles, histograms, pixel values, measurements, and image channels.
- Copy image-window screenshots as PNG directly to the clipboard.
- Keep Visual Studio responsive with lazy file loading and safe previews for large objects.

## Why It Exists

HALCON is excellent inside HDevelop. C# debugging needs a faster bridge between the breakpoint and the actual HALCON data.

This tool focuses on a short debugging loop:

```text
Stop at breakpoint -> open variable -> inspect object -> continue debugging
```

It is built for algorithm engineers who need to verify real intermediate variables without exporting every object by hand.

## Highlights

| Area | Capability |
|---|---|
| Visual Studio debugging | Open HALCON variables from the debugger magnifier |
| Standalone viewing | Drag files and folders into the viewer |
| Image inspection | Channel switch, pixel readout, zoom, pan, fit |
| Region overlay | Fixed LUT-style colors, fill or contour mode |
| Analysis tools | Distance measurement, grayscale profile, histogram |
| Workflow | Copy PNG screenshot directly to clipboard |
| Large data | Lazy file loading and safe previews reduce UI stalls |

## Requirements

- Windows.
- Visual Studio 2022.
- .NET Framework 4.7.2 or later.
- HALCON Runtime and a valid HALCON license for reading native HALCON files such as `.hobj`, `.tup`, and `.hdict`.

Plain image files and `.hvx` snapshots do not require HALCON Runtime.

## Updates

The viewer reads:

```text
update/latest.json
```

When a newer version is published, the in-app update button downloads the installer, verifies SHA256, then launches the installer.

Public release layout:

```text
update/latest.json
downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe
```

## Repository Scope

This public repository is a binary distribution and update channel. It contains:

- Public update manifest.
- Public installer artifacts.

It does not contain the private source code.

## Notes

The installer does not include HALCON Runtime, HALCON configuration, or license files. Target machines must provide their own HALCON environment when native HALCON file loading is needed.
