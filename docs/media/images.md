---
layout: default
title: Images
parent: Media commands
nav_order: 1
---

# Images
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Resize images

```bash
mogrify -resize x1920 *.jpg
mogrify -resize 320x240 *.png
mogrify -resize 50% *.png
mogrify -resize 320x240 *.jpg
```
