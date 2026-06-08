# HALCON Variable Inspector / HALCON 变量查看器

<p align="center">
  <strong>Inspect HALCON images, regions, tuples, and dictionaries directly from a C# breakpoint.</strong>
  <br>
  <span>面向 Visual Studio 2022 + C# + HALCON 调试场景的变量查看器。</span>
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
  <a href="#what-it-does">Features</a>
  ·
  <a href="#requirements">Requirements</a>
  ·
  <a href="#updates">Updates</a>
</p>

---

```text
C# Breakpoint
    -> Visual Studio magnifier
        -> HALCON image / region / dict / tuple viewer
            -> inspect, measure, copy screenshot, continue debugging
```

## Download

Install the latest public build:

<p>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><strong>Download HalconVariableInspectorSetup-1.0.3.exe</strong></a>
</p>

Current public update manifest:

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

The installer places the Visual Studio debugger visualizer and the standalone viewer into the current user's Visual Studio 2022 Visualizers directory.

## What It Does

HALCON Variable Inspector turns C# debugging into an inspection workspace for HALCON variables:

- Open `HObject`, `HImage`, `HRegion`, `HXLDCont`, `HTuple`, and `HDict` directly from Visual Studio Watch, Locals, or Autos.
- View images, regions, and XLD overlays with fixed LUT-style region colors.
- Drag local `.hobj`, `.tup`, `.hdict`, `.hvx`, image files, or folders into the standalone viewer.
- Inspect grayscale profiles, histograms, pixel values, measurements, channels, and copied screenshots without saving temporary files.
- Keep Visual Studio responsive through lazy file loading and safe previews for large objects.

## Why It Exists

HALCON's native tools are strong inside HDevelop, but C# debugging often needs a faster bridge.

```text
Breakpoint -> magnifier -> inspect image/region/dict -> continue debugging
```

This tool focuses on that loop. It is built for algorithm engineers who need to verify real intermediate variables without exporting every object by hand.

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

The viewer checks:

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
