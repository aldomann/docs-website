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

2. Install Wine if required:
```bash
sudo pacman -S wine --needed
```
To accept the License agreement, press Tab + Enter.

3. Install winetricks if required:
```bash
sudo pacman -S winetricks --needed
```

4. Install `adobe_diged4` on a 32bit-environment:
```bash
export WINEPREFIX=~/.wine32-ade
WINEARCH=win32 wine wineboot
winetricks adobe_diged4
```

## Install DeDRM Tools (ADE)

<span class="fs-3">
[Source A](https://github.com/apprenticeharper/DeDRM_tools/releases){: .btn .btn-purple .mr-2 }
[Source B](https://apprenticealf.wordpress.com/){: .btn .btn-purple .mr-2 }
[Source C](http://www.voidspace.org.uk/python/modules.shtml#pycrypto){: .btn .btn-purple .mr-2 }
</span>

1. Generate Encryption Key
```bash
winetricks python
```

1. Download and install PyCrypto:
```bash
wine pycrypto-2.6.win32-py2.6.exe
```

1. Generate ADE Encryption key:
```
cd DeDRM_tools_6.5.5/Other_Tools/DRM_Key_Scripts/Adobe_Digital_Editions
wine /home/aldomann/.wine32-ade/drive_c/Python26/python.exe adobekey.pyw
```

## SketchUp 2018

<span class="fs-3">
[Source](https://appdb.winehq.org/objectManager.php?sClass=version&iId=34500&iTestingId=99793){: .btn .btn-purple .mr-2 }
</span>

1. Install Wine if required:
```bash
sudo pacman -S wine --needed
```
To accept the License agreement, press Tab + Enter.

2. Install winetricks if required:
```bash
sudo pacman -S winetricks --needed
```

3. Set up WINEPREFIX for a 64bit-environment:
```bash
export WINEARCH=win64
export WINEPREFIX=~/.wine-sketchup
wine wineboot
```

4. Download [.NET Framework 4.7 (offline version)](https://www.microsoft.com/en-us/download/details.aspx?id=55167) and install it with the following command:
```bash
wine start /unix NDP47-KB3186497-x86-x64-AllOS-ENU.exe
```

5. Finally, run the actual SketchUp installer:
```bash
wine Setup.exe
```
