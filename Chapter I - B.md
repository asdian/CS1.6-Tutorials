# Chapter I: Section B - MetaHook
Guide to install MetaHookSv and Its Third Party Plugins.
> [!NOTE]
> This is a bit complicated step, make sure you followed carefully. A slight miss can lead to game crash/unstable.
> Don't rush it, take your time.

## $\color{BlueGreen}{MetaHookSv}$
#### $\color{Apricot}{What\ is\ Metahook?}$
Metahook is an addon for Goldsrc-based games to give extensive functionality (like ReHLDS and such). It works by using a special launcher that renames itself to match the game's executable, such as cstrike.exe, then loads the real game while injecting its own DLL early in the process. This DLL hooks into the engine's core functions, like rendering and input, using techniques such as inline patches and virtual table replacements. Once hooked, MetaHook loads plugins from a folder as DLL files, allowing them to add features like custom HUDs, improved lighting, shaders, and modern graphics effects. Because of that, Metahook is heavily dependent with newer OpenGL and DirectX system, with moderate system specification (just to be safe). Unfortunately as I wrote this guide, Metahook is for Windows only, which is have its specific requirements to be used for multiplayer/online mode (don't ask me how, I don't know either).

Very first MetaHook version is just "MetaHook" developed by Nagist. There's also "MetaHook Plus" version, I assume it's Nagist's fork for CS:BTE family of games. And finally, the latest and actively maintained version is "MetaHookSv" developed by hzqst, which is the one I'm using. It's originally developed for Svencoop, but it can be used for CS1.6 as well. MetaHookSv comes with its own set of plugins. [The plugin list](https://github.com/hzqst/MetaHookSv/blob/main/docs/Plugins.md)

#### $\color{GreenYellow}{System\ Requirements}$
- Read more [Here](https://github.com/hzqst/MetaHookSv/blob/main/docs/Renderer.md#gpu-requirement).

#### $\color{GreenYellow}{Installation\ Steps}$
1. Download MetaHookSv from [here](https://github.com/hzqst/MetaHookSv/releases). 
> [!IMPORTANT]
> - For 3266 game build, <ins>choose blob.</ins> 

2. Copy `cstrike_hd`, `echoes`, `gearbox`, `platform`, `Metahook.exe` or `Metahook_blob.exe`, `SDL2.dll`, and `SDL3.dll` into your installed CS1.6 folder.
3. Open `svencoop` folder and copy everything into `cstrike` folder.
4. Back to your installed CS1.6 folder, rename the original `cstrike.exe` to something else if exist (as a backup).
5. Rename <ins>`Metahook.exe`(latest CS)</ins> or <ins>`Metahook_blob.exe`(for 3266)</ins> to `cstrike.exe`
6. Go to `cstrike\metahook\configs` folder, delete `plugins_svencoop.lst` and rename `plugins_goldsrc.lst` to `plugins.lst`.
7. Run and play your CS1.6 from `cstrike.exe`, play with built-in/addon bots if any, make sure eveything runs fine, no crash. If you're facing crashes and other, might be your installment/system issue.
8. Inside the game, press tilde `~` symbol on your keyboard, then type _`mh_pluginlist`_. If the output matches what's shown in the image below (or something similar), the Metahook is successfully installed.

![List of installed Metahook Plugins.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/BaseGame/status-mh.png)

## $\color{BlueGreen}{Third\ Party\ Plugins}$ 
The plugins listed here are the plugins I have tried and used. When you have done installing third-party plugins, continue to [AMX Mod X installation](Chapter%20I%20-%20C.md). **Some Metahook plugins may need AMX Mod X to be installed first.

#### $\color{GreenYellow}{General\ installation}$
Metahook plugin installation is generally the same.
1. Download the plugin.
2. Find and copy the `.dll` file into `cstrike\metahook\plugins`.
3. Open `cstrike\metahook\configs\plugins.lst` with any text editor.
4. Write the `.dll` file name you just copied from the package (with the `.dll` text) on the very top of the list, then save it.
5. Read any additional info/steps if there's any.
6. Start the game and make sure the new Metahook plugin is listed after you're typing _`mh_pluginlist`_.

### $\color{ProcessBlue}{Client\ Precache\ (build\ 3266\ only)}$
> [!WARNING]
> The latest MetaHookSv version that supports this plugin is [v20250225b](https://github.com/hzqst/MetaHookSv/releases/tag/v20250225b). If you have already installed a newer version, please roll back to v20250225b to avoid issues.

Client Precache is a MetaHook Plugin to increase precache limit (you read it right) to around ~1024. I'm not quite sure how it works since it's closed source. Unfortunately this plugin only designed specifically for build 3266. That's why I mention build 3266 in the first place and specific MetaHookSv version to be installed.

1. Download from [here](https://www.mediafire.com/file/nh8ui1ht070k96u/MH_Precache.rar/file) then install as written on the guide above.
2. Open `cstrike\delta.lst` with any text editor.
3. Find every parameter that contains `modelindex`, `viewmodel`, `weaponmodel`, then change the value from `10` to `16`, and save it.

### $\color{ProcessBlue}{Metadrawer}$
> [!CAUTION]
> As of now (2026/02/27) any of these plugins under this point are <ins>NOT</ins> compatible with latest release of MetaHookSv's first party plugins. You have to clear `plugins.lst` first. I'm not sure which plugins that causes the crash. If you're using v20250225b version, it still can run fine. No need to clear `plugins.lst` first.

Metadrawer is a MetaHook Plugin to give extensive functionality that normal AMX Mod X can't do, such as drawing image in-game.

0. Requires full [AMX Mod X installation](Chapter%20I%20-%20C.md).
1. Download from [here](https://gamebanana.com/mods/39420).
2. Backup your `cstrike\metahook\configs\plugins.lst` (just in case).
3. Place `binkw32.dll` and `cstrike` folder into your installed CS1.6 folder. $\color{Red}{**}$ Metadrawer package will replace `plugins.lst` with its own file if you place the entire `cstrike` folder, unless you want to do it manually.
4. Restore your `cstrike\metahook\configs\plugins.lst`.
5. Install as written on the guide above. 
6. Go to cstrike folder, create a file named _`userconfig.cfg`_ (a must, can't use random naming). Not a .txt file, make sure you have done that properly.
7. Write this command: _`md_newmenu "0"`_ inside and save it.


> [!TIP]
> Alternatively, you can use [MetaInvoker](https://csumods.blogspot.com/2026/01/cs16-plugin-metahook-metainvoker-03.html) which provides around the same features. But don't mix them unless you're know what you're doing.

### $\color{ProcessBlue}{MetaCCX}$
My personal and first MetaHookSv which aimed to be complementary of my CCX plugin of AMX Mod X. As of now, it gives HUD enhancements mimicking CSO/CSN:S.

1. ~~Download from [here] and install as written on the guide above~~ Soon!
2. Extract the files.