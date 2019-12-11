---
layout: default
title: Games
parent: Installation guides
nav_order: 3
---

# Games
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Age of Empires II: HD on Steam
1. Enable Proton on Steam.
	- Go to Account Settings.
	- Enable Steam Play.

2. Install [Age of Empires II: HD](https://store.steampowered.com/app/221380/Age_of_Empires_II_2013/).

3. Rename `AoK.exe` to `Launcher.exe`:

```bash
cd $HOME/.local/share/Steam/steamapps/common/Age2HD
mv Launcher.exe Launcher_backup.exe
cp AoK\ HD.exe Launcher.exe
```

*Notice that instead of `~/.local/share/Steam`, your Steam Library could be located in `~/.SteamLibrary`*.

## Civilization IV on Steam

1. Enable Proton on Steam.
	- Go to Account Settings.
	- Enable Steam Play.
2. Install [Sid Meier's Civilization® IV](https://store.steampowered.com/sub/4323/). Notice that you'll only need to install the latest expansion (Beyond the Sword).

3. Remove the `8800` directory.

4. Recreate the Wine prefix by using the "Verify Integrity of Game Files" feature.

5. Install `msxml3`:
```bash
WINEPREFIX=~/.local/share/Steam/steamapps/compatdata/8800/pfx WINE=~/.local/share/Steam/steamapps/common/Proton\ 3.7/dist/bin/wine winetricks msxml3
```

6. Install `msxml4`:
```bash
WINEPREFIX=~/.local/share/Steam/steamapps/compatdata/8800/pfx WINE=~/.local/share/Steam/steamapps/common/Proton\ 3.7/dist/bin/wine winetricks msxml4
```

*Notice that instead of `~/.local/share/Steam`, your Steam Library could be located in `~/.SteamLibrary`*.

