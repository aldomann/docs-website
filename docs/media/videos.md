---
layout: default
title: Videos
parent: Media commands
nav_order: 3
---

# Videos
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Remove subtitles from MKV

Assume we have `input.mkv` with 3 subtitle tracks. The following command removes subtitle track 2 by copying tracks 1 & 3 from `input.mkv` and saving it to `output.mkv`:

```bash
mkvmerge -o output.mkv --subtitle-tracks 1,3 input.mkv
```
