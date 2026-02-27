# Chapter I
## Guide to set up the base game.

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

If you done, continue to [Chapter II](https://github.com/asdian/CS1.6-Tutorials/blob/main/Chapter%20II.md)
.
6. Now download this Metahook plugin from [here](https://www.mediafire.com/file/nh8ui1ht070k96u/MH_Precache.rar/file).
7. Find and copy the `.dll` file into `cstrike\metahook\plugins`.
8. Open `cstrike\metahook\configs\plugins.lst` with any text editor.
9. Write the `.dll` file name you just copied from the .rar (with the `.dll` text) and save it.
10. Open `cstrike\delta.lst` with any text editor.
11. Find every parameter that contains `modelindex`, `viewmodel`, `weaponmodel`, then change the value from `10` to `16`, and save it.
12. Repeat step 3-5. Make sure the new Metahook plugin is listed after you're typing _`mh_pluginlist`_.

<a name="why-must-3266"></a>
> [!NOTE]
> #### Why specific 3266 build is required?
> The Metahook plugin we're going to use is to extend the precache limit (you read it right). But currently it only works with build 3266. That's why it requires build 3266, which is quite hard to find nowadays. Thanks to archive.org I can find one that easy to download and install without crappy files (clean). If you're not intended to use this Metahook plugin, you can use another or newer build and can follow this guide just fine, skipping step 6 and beyond.

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
