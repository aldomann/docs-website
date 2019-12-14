---
layout: default
title: Installing Git
parent: Git
nav_order: 1
---

# Installing Git
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## On GNU/Linux

On any decent Linux distribution, Git should be installed by default (yeah, looking at you Ubuntu). If that’s not the case, you can just install it from your terminal:

### Debian/Ubuntu derivatives
```bash
sudo apt install git
```

### Arch Linux
```bash
sudo pacman -S git
```

### Fedora
```bash
sudo dnf install git
```

## On mac OS

To have git (and gcc, and many other developer tools), you must have XCode (or XCode Command Line Tools) on your system, so just head to the App Store and install it. Expect to waste half your afternoon, as it is around 6 GB to download, and then it needs to be installed.

```bash
xcode-select install
```

## On Windows

I’m not familiar with the system so I won’t bother. You’re on your own. ¯\\\_(ツ)\_/¯
