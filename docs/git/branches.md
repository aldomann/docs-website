---
layout: default
title: Branches
parent: Git
nav_order: 4
---

# Branches
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Create local branch
```bash
git checkout -b <local-branch>
```

## Push current local branch to remote
```bash
git push origin <remote-branch>
```

## Sync remote branch to current local
```bash
git pull origin <remote-branch>
```

## Set permanent local-remote link
```bash
git branch --set-upstream-to=origin/<remote-branch> <local-branch>
```



## Delete remote branch
```bash
git push origin --delete <remote-branch>
```

## Delete local branch
```bash
git branch -D <local-branch>
```
