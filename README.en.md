# HALCON Variable Inspector

<p align="center">
  <strong>A Visual Studio 2022 + C# + HALCON variable inspection cockpit.</strong>
  <br>
  <span>Open real HALCON runtime objects from a breakpoint, then inspect images, regions, tuples, dictionaries, and local variable files.</span>
</p>

<p align="center">
  <a href="README.md">中文</a>
  ·
  <a href="README.en.md"><strong>English</strong></a>
</p>

<p align="center">
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><img alt="Download v1.0.3" src="https://img.shields.io/badge/Download-v1.0.3-21b8a6?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json"><img alt="Update channel" src="https://img.shields.io/badge/Update-stable-0f172a?style=for-the-badge"></a>
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

## Download

<p>
  <a href="https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe"><strong>Download HalconVariableInspectorSetup-1.0.3.exe</strong></a>
</p>

The installer places the Visual Studio debugger visualizer, standalone viewer, uninstaller, and update support into the current user's Visual Studio 2022 Visualizers directory.

```text
C:\Users\<User>\Documents\Visual Studio 2022\Visualizers
```

## Debugging Loop

| Stage | What engineers see | What the tool does |
|---|---|---|
| Breakpoint | HALCON variables in Watch, Locals, or Autos | Opens the real variable through the magnifier |
| Expansion | `HObject`, `HImage`, `HRegion`, `HTuple`, `HDict` | Creates a visualization snapshot and launches Viewer |
| Image inspection | Channels, pixel values, zoom, pan, fit | Keeps interaction responsive without blocking VS |
| Region overlay | Fixed LUT-style colors, fill, contour | Displays object regions in a stable order |
| Review | Profile, histogram, measurement, snapshot copy | Sends debugging evidence straight to the clipboard |

## Capability Matrix

| Capability | Description |
|---|---|
| VS debugger magnifier | Open HALCON variables from a C# breakpoint without temporary export code |
| Standalone file viewer | Drag `.hobj`, `.tup`, `.hdict`, `.hvx`, images, and folders into Viewer |
| Region visualization | Fixed LUT-style color sequence for Region and XLD overlays |
| Image analysis | Single-channel, multi-channel, pixel readout, grayscale profile, histogram |
| Workflow output | Copy image-window screenshots directly to the clipboard as PNG |
| Large-object protection | Lazy loading and safe previews reduce UI stalls |
| Update channel | Reads a public manifest, verifies SHA256, then launches the installer |

## Why It Matters

HALCON is strong inside HDevelop, but C# debugging often splits the real runtime variable and the visual judgment into different tools.

This Viewer shortens the loop:

```text
Pause -> open variable -> inspect image and region -> judge algorithm state -> continue debugging
```

It is built for algorithm engineers, not for generic photo browsing. The focus is accurate HALCON variable loading, stable region display, fast channel switching, and keeping Visual Studio responsive.

## Requirements

| Item | Requirement |
|---|---|
| OS | Windows x64 |
| IDE | Visual Studio 2022 |
| Runtime | .NET Framework 4.7.2 or later |
| Native HALCON files | Reading `.hobj`, `.tup`, and `.hdict` requires HALCON Runtime and a valid HALCON license on the target machine |
| Plain images and snapshots | Image files and `.hvx` snapshots do not require HALCON Runtime |

## Updates

Viewer reads the public version manifest:

```text
https://raw.githubusercontent.com/tangao1112/halconvisualizer-public/main/update/latest.json
```

Release layout:

```text
update/latest.json
downloads/v1.0.3/HalconVariableInspectorSetup-1.0.3.exe
```

When a newer version is available, the in-app update button downloads the installer, verifies SHA256, then launches the installer. This public repository only provides binary installers and update metadata.

## Repository Scope

This repository is a public distribution channel. It contains:

| Content | Included |
|---|---|
| Installer | Yes |
| Update manifest | Yes |
| Private source code | No |
| HALCON Runtime | No |
| HALCON license files | No |

Target machines must provide their own HALCON Runtime, configuration, and license. The installer does not modify HALCON configuration on the target machine.
