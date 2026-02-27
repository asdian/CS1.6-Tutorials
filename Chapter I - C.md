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
9. Inside the game, press tilde `~` symbol on your keyboard, then type _`meta list`_ and _`amxx plugins`_. If the output shows as shown on this image below or similar (outputs something, not an unknown command), the package is successfully installed.

![Metamod installed plugin list.](https://github.com/asdian/CS1.6-Tuts/blob/main/Pics/BaseGame/Screenshot_2.png)

10. Make sure the game is stable. Play for few minutes or hours to make sure. Also try to change maps, change teams, change classes, etc.

## C. ReGameDLL
Read the details [here](https://github.com/rehlds/ReGameDLL_CS).

### Installation Steps
1. Download either [Dev Build](https://github.com/rehlds/ReGameDLL_CS/actions/workflows/build.yml) or [Release Build](https://github.com/rehlds/ReGameDLL_CS/releases) (not both).
2. Inside the .zip file, go to `bin\win32` folder then place `cstrike` folder into your CS1.6 directory.
3. For latest game version, you can use its built-in bot (ZBot) [here](https://github.com/rehlds/ReGameDLL_CS?tab=readme-ov-file#how-to-install-zbot-for-cs-16) or CS:CZ Hostage AI [here](https://github.com/rehlds/ReGameDLL_CS?tab=readme-ov-file#how-to-install-cscz-hostage-ai-for-cs-16)

## D. ReAPI
From what I can understand, ReAPI is a bridging module between ReGameDLL and AMX Mod X. It lets modder/developer to use ReGame abilities from AMX Mod X.

### Installation Steps.
1. Download either [dev build](https://github.com/rehlds/ReAPI/actions) or [release build](https://github.com/rehlds/ReAPI/releases).
2. Open the .zip, and place `addons` folder to your `cstrike` folder.

***
Now, run the game again. Play for few minutes or hours. Change maps, change team, change class, to test everything. Check the game console (by pressing tilde `~` icon, below `esc` button), then type _`meta list`_ and _`amxx plugins`_. If the output shows as shown on this image below or similar (outputs something, not an unknown command), the AMX Mod X and its complimentary addons are successfully installed.

![Metamod installed plugin list.](https://github.com/asdian/CS1.6-Tuts/blob/main/Pics/BaseGame/Screenshot_2.png)