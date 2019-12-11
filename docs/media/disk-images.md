---
layout: default
title: Disk images
parent: Media commands
nav_order: 5
---

# Disk images
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## List drives

To view a list of all drives currently attached to your system run:

```bash
sudo fdisk -l
```

## Create a LiveUSB

To write the Live Install image to your USB, run the following command:
```bash
sudo dd bs=4M if=/path/to/antergos-x86_64.iso of=/dev/sdX && sync
```

## Mount an ISO image

To mount an ISO image on a virtual disk, run the following command:

```bash
udisksctl loop-setup -r -f image.iso
```
