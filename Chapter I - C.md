# Chapter I: Section C - AMX Mod X
## Guide to install AMX Mod X and Its Complementary Addons

## A. Metamod
Metamod (often just called "Metamod") is a plugin loader / manager originally created for games using the GoldSrc engine (like Half-Life 1 and Counter-Strike 1.6). It acts as a middleware layer that sits between the game engine and the actual game mod (the game DLL), allowing server owners to dynamically load and unload additional plugin DLLs without modifying the core game files. This made it possible to add custom server features, admin tools, anti-cheat systems, bots, fun commands, statistics, etc.

### Installation steps
1. There are two differences. Choose one.
> For build 3266, download Metamod-P from [here](https://github.com/Bots-United/metamod-p/releases).\
> For latest build, download Metamod-R from [here](https://github.com/rehlds/Metamod-R/releases).

2. Inside `cstrike` folder, create new folder and name it `addons`.
3. Inside `addons` folder, create new folder again and name it `metamod`.
4. Place `metamod.dll` into `metamod` folder you just created.
5. Back to `cstrike` folder, open `liblist.gam` with any text editor.
6. Find `gamedll` entry, then change its string into `"addons\metamod\metamod.dll"` (with quote).
7. Save and close.

## B. AMX Mod X
AMX Mod X (often abbreviated AMXX) is a powerful scripting and server administration framework designed as a Metamod plugin for Half-Life 1 (GoldSrc engine) games, most famously Counter-Strike 1.6. It lets server admins and developers create custom plugins to add features like admin commands (kick/ban/slay/reservations), voting systems, anti-flood, stats tracking, weapon restrictions, custom game modes, bots, and much more—without touching the core game files.

### Installation steps
1. Go to this [website](https://www.amxmodx.org/downloads-new.php?branch=master&all=1).
2. Click Windows icon, download both `base` and `cstrike` package.
3. Open `base` package, and extract `addons` folder into `cstrike` folder.
4. Do the same with `cstrike` package.
5. Go to `cstrike/addons/metamod` folder, open `plugins.ini` using text editor. Create one if doesn't exist.
6. Write this entry: `win32   addons\amxmodx\dlls\amxmodx_mm.dll`
7. Save and close.
8. Start and run the game.
9. Inside the game, press tilde `~` symbol on your keyboard, then type _`meta list`_ and _`amxx plugins`_. If the output shows as shown on this image below or similar (outputs something, not an unknown command), the package is successfully installed.

![Metamod installed plugin list.](https://github.com/asdian/CS1.6-Tuts/blob/main/Pics/BaseGame/Screenshot_2.png)

10. Make sure the game is stable. Play for few minutes or hours to make sure. Also try to change maps, change teams, change classes, etc.

## C. ReGameDLL
Read the details [here](https://github.com/rehlds/ReGameDLL_CS).

### Installation Steps
1. Download either [Dev Build](https://github.com/rehlds/ReGameDLL_CS/actions/workflows/build.yml) or [Release Build](https://github.com/rehlds/ReGameDLL_CS/releases) (not both).
2. Inside the .zip file, go to `bin\win32` folder then place `cstrike` folder into your CS1.6 directory.
3. For latest game version, you can use its built-in bot (ZBot) [here](https://github.com/rehlds/ReGameDLL_CS?tab=readme-ov-file#how-to-install-zbot-for-cs-16) or CS:CZ Hostage AI [here](https://github.com/rehlds/ReGameDLL_CS?tab=readme-ov-file#how-to-install-cscz-hostage-ai-for-cs-16)

### How to Enable SyPB
1. Open `cstrike/addons/metamod/plugins.ini`.
2. On _`;win32   addons\sypb\dlls\sypb.dll`_ line, delete the semicolon `;` and then save it. If that line doesn't exist just copy-paste it without the semicolon.
3. Open `cstrike/addons/amxmodx/configs/modules.ini`.
4. Find these two lines: _`;sypb`_ and _`;swnpc`_.
5. Delete the semicolon `;` from them and then save it. If those lines doesn't exist just write them without the semicolon. _**Don't write them at the same line.**_
6. On the game lobby, make sure to disable the built-in bot.

![Disable zbot.](https://github.com/asdian/CS1.6-Tuts/blob/main/Pics/BaseGame/Screenshot_3.png)

7. Repeat the step 3 of [Setting up the base game.](https://github.com/asdian/CS1.6-Tuts/blob/main/CS1.6%20Base%20Game%20Tut.md#setting-up-the-base-game).

> Congratulations!
> -
> Now you have a working base game to start modding. You don't have to worry with 512 precache limit again thanks to that Metahook plugin. It increases the precache to around 1024.
---
