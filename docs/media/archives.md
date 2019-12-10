---
layout: default
title: Archives
parent: Media commands
nav_order: 4
---

# Archives
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Compress each file in a different 7-Zip archive
```bash
for X in *; do 7z a -t7z -mx9 "$X".7z "$X"; done
```

## Compress each folder in a different ZIP archive
```bash
for i in */; do zip -r "${i%/}.zip" "$i"; done
```
