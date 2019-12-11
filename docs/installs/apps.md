---
layout: default
title: Apps
parent: Installation guides
nav_order: 2
---

# Apps
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Adobe Digital Editions (Wine)

<span class="fs-3">
[Source](https://appdb.winehq.org/objectManager.php?sClass=version&iId=33276){: .btn .btn-purple .mr-2 }
</span>

1. Install the `winbind` package, if not yet done:
```bash
sudo pacman -S libwbclient --needed
```

1. Install Wine if required:
```bash
sudo pacman -S wine --needed
```
To accept the License agreement, press Tab + Enter.

1. Install winetricks if required:
```bash
sudo pacman -S winetricks --needed
```

1. Install `adobe_diged4` on a 32bit-environment:
```bash
export WINEPREFIX=~/.wine32-ade
WINEARCH=win32 wine wineboot
winetricks adobe_diged4
```

## Install DeDRM Tools (ADE)

<span class="fs-3">
[Source A](https://github.com/apprenticeharper/DeDRM_tools/releases){: .btn .btn-purple .mr-2 }
[Source B](https://apprenticealf.wordpress.com/){: .btn .btn-purple .mr-2 }
</span>

1. Generate Encryption Key
```bash
winetricks python
```

1. Download and install PyCrypto:
SRC: http://www.voidspace.org.uk/python/modules.shtml#pycrypto
```bash
wine pycrypto-2.6.win32-py2.6.exe
```

1. Generate ADE Encryption key:
```
cd DeDRM_tools_6.5.5/Other_Tools/DRM_Key_Scripts/Adobe_Digital_Editions
wine /home/aldomann/.wine32-ade/drive_c/Python26/python.exe adobekey.pyw
```

## SketchUp 2018

```bash
echo "Hello world!"
```
