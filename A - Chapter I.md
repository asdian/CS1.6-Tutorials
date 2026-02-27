# Chapter I - Base Game Setup

### System Requirements
- The same as listed from [CS1.6 Steam Page](https://store.steampowered.com/app/10/CounterStrike/)
- Video card / graphics that supports DX11 and OpenGL 4.2+

### Setting up the base game.
Choose between build 3266 or Latest version.

## $\color{Cyan}{[Build\ 3266]}$ 
1. Download CS1.6 build 3266 from [here](https://archive.org/details/counter-strike-1.6_202106). (Why? You will find it later.)
2. Install it to your desired folder
3. Play for few minutes or hours to make sure. Also try to change maps, change teams, change classes, etc.

## $\color{Cyan}{[Latest\ Build]}$
1. Buy from Steam store [here](https://store.steampowered.com/app/10/CounterStrike/).
2. Download and install to your desired folder
3. Play for few minutes or hours to make sure. Also try to change maps, change teams, change classes, etc.
4. Steam version doesn't come with bot option by default. You have to install bot addon yourself.

When you done, continue to [Chapter II](https://github.com/asdian/CS1.6-Tutorials/blob/main/Chapter%20II.md).

### Installing Metadrawer [Optional]
Optionally, you can install Metadrawer, a Metahook plugin to load images for UI enhancements into the game.

1. Download from [here](https://gamebanana.com/mods/39420).
2. Place `binkw32.dll` and `cstrike` folder into your installed CS1.6 folder.
3. Open `cstrike\metahook\configs\plugins.lst` with any text editor.
4. Write that .dll file name you just copied and save it.
5. Go to cstrike folder, create a file named _`userconfig.cfg`_ (a must, can't use random naming). Not a .txt file, make sure you have done that properly.
6. Write this command: _`md_newmenu "0"`_ inside and save it.
7. Go to `cstrike\addons\amxmodx\configs` folder, open `modules.ini` with any text editor, write _`metadrawer`_ in it and save.
8. Repeat the step 3-5 of [Setting up the base game.](https://github.com/asdian/CS1.6-Tuts/blob/main/CS1.6%20Base%20Game%20Tut.md#setting-up-the-base-game).

> [!TIP]
> Alternatively, you can use [MetaCSU](https://csumods.blogspot.com/2023/06/cs16-plugin-metahook-mhmetacsu-v02.html) which provides around the same functionality. But don't mix them unless you're know what you're doing.

> That's all, you have successfully installed a CS1.6 complete with its addons for modding.
> -
