# Chapter I: Section B - MetaHook
## Guide to install MetaHookSv and Its Third Party Plugins.

> [!WARNING]
> This is a bit complicated step, make sure you followed carefully. A slight miss can lead to game crash/unstable.
> Don't rush it, take your time.

### What is Metahook?
Metahook is an addon for Goldsrc-based games to give extensive functionality (like ReHLDS and such). It works by using a special launcher that renames itself to match the game's executable, such as cstrike.exe, then loads the real game while injecting its own DLL early in the process. This DLL hooks into the engine's core functions, like rendering and input, using techniques such as inline patches and virtual table replacements. Once hooked, MetaHook loads plugins from a folder as DLL files, allowing them to add features like custom HUDs, improved lighting, shaders, and modern graphics effects. Because of that, Metahook is heavily dependant with newer OpenGL and DirectX system, with moderate system specification (just to be safe). Unfortunately Metahook is for Windows only, which is have its specific requirements to be able to use for multiplayer/online mode (don't ask me how, I don't know either). 

### System Requirements
- Read more [Here](https://github.com/hzqst/MetaHookSv/blob/main/docs/Renderer.md#gpu-requirement).

### Installation Steps
1. Download MetaHookSv from [here](https://github.com/hzqst/MetaHookSv/releases). 
> [!CAUTION]
> For 3266 game build, use this specific version [here](https://github.com/hzqst/MetaHookSv/releases/tag/v20250225b). $\color{Yellow}{[}$ $\color{RedOrange}{Important\ !}$ $\color{Yellow}{]}$ <ins>Choose blob.</ins> 

2. Copy `cstrike_hd`, `echoes`, `gearbox`, `platform`, `Metahook_blob.exe`, `SDL2.dll`, and `SDL3.dll` into your installed CS1.6 folder.
3. Open `svencoop` folder and copy everything into `cstrike` folder.
4. Back to your installed CS1.6 folder, rename the original `cstrike.exe` to something else if exist (as a backup).
5. Rename <ins>`Metahook.exe`(latest CS)</ins> or <ins>`Metahook_blob.exe`(for 3266)</ins> to `cstrike.exe`
6. Go to `cstrike\metahook\configs` folder, delete `plugins_svencoop.lst` and rename `plugins_goldsrc.lst` to `plugins.lst`.
7. Run and play your CS1.6 from `cstrike.exe`, play with built-in/addon bots, make sure eveything runs fine, no crash. If you're facing crashes and other, might be your installment/system issue.
8. Inside the game, press tilde `~` symbol on your keyboard, then type _`mh_pluginlist`_. If the output shows as shown on this image below, the Metahook is successfully installed.

![List of installed Metahook Plugins.](https://github.com/asdian/CS1.6-Tuts/blob/main/Pics/BaseGame/Screenshot_1.png)

## Third Party Plugins

### A. Client Precache (build 3266 only)
Client Precache is a MetaHook Plugin to increase precache limit (you read me right). I'm not quite sure how it works since it's closed source. Unfortunately this plugin only designed specifically for build 3266. That's why I mention build 3266 in the first place and specific MetaHookSv version to be installed.

1. Download from [here](https://www.mediafire.com/file/nh8ui1ht070k96u/MH_Precache.rar/file).
2. Find and copy the `.dll` file into `cstrike\metahook\plugins`.
3. Open `cstrike\metahook\configs\plugins.lst` with any text editor.
4. Write the `.dll` file name you just copied from the .rar (with the `.dll` text) on the very top of the list, then save it.
5. Open `cstrike\delta.lst` with any text editor.
6. Find every parameter that contains `modelindex`, `viewmodel`, `weaponmodel`, then change the value from `10` to `16`, and save it.
7. Repeat step 3-5. Make sure the new Metahook plugin is listed after you're typing _`mh_pluginlist`_.

