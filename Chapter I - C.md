---
### Installing AMX Mod X
Now, on to installation of AMX Mod X.

1. Download this [package](https://github.com/asdian/CS1.6-Singleplayer-Setup/blob/main/AMX%20Mod%20X%20Starter%20Pack.rar). It contains ReGameDLL 5.26.0.668-dev, SyPB 1.50 (disabled by default), Metamod-P 1.21p38, Printcenter fix, and AMXModX 1.10.0.5467.
2. Extract all the files into _`cstrike`_ folder. ***If you're using aforementioned Metahook plugin, repeat step 8-11 above.**
3. Start and run the game.
4. Inside the game, press tilde `~` symbol on your keyboard, then type _`meta list`_ and _`amxx plugins`_. If the output shows as shown on this image below or similar (outputs something, not an unknown command), the package is successfully installed.

![Metamod installed plugin list.](https://github.com/asdian/CS1.6-Tuts/blob/main/Pics/BaseGame/Screenshot_2.png)

5. Make sure the game is stable first before continuing. Play for few minutes or hours to make sure. Also try to change maps, change teams, change classes, etc.

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
