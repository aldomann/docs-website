---
layout: default
title: Media commands
nav_order: 2
---

# Media commands
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Images {#images}

```bash
mogrify -resize x1920 *.jpg
mogrify -resize 320x240 *.png
mogrify -resize 50% *.png
mogrify -resize 320x240 *.jpg
```


## Audio {#audio}

### Cut MP3 file

```bash
mp3cut -o output.mp3 -t 00:00:20+000-00:00:58+000 input.mp3
```

## Videos {#videos}

### Remove subtitles from MKV

Assume we have `input.mkv` with 3 subtitle tracks. The following command removes subtitle track 2 by copying tracks 1 & 3 from `input.mkv` and saving it to `output.mkv`:

```bash
mkvmerge -o output.mkv --subtitle-tracks 1,3 input.mkv
```

## Archives {#archives}

### Compress each file in a different `.7z`
```bash
for X in *; do 7z a -t7z -mx9 "$X".7z "$X"; done
```

### Compress each folder in a different `.zip`
```bash
for i in */; do zip -r "${i%/}.zip" "$i"; done
```

## Disk Images

### Mount an ISO image

To mount an ISO image on a virtual disk, run the following command:

```bash
udisksctl loop-setup -r -f image.iso
```

### Create a LiveUSB
To write the Live Install image to your USB, run the following command:
```bash
sudo dd bs=4M if=/path/to/antergos-x86_64.iso of=/dev/sdX && sync
```