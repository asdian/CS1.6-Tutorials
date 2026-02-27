# Chapter II
## Guide to install MetaHookSv and Its Third Party Plugins.

> [!WARNING]
> This is a long step, make sure you followed carefully. A slight miss can lead to game crash/unstable.
> Don't rush it, take your time.

### System Requirements
- The same as listed from [CS1.6 Steam Page](https://store.steampowered.com/app/10/CounterStrike/)
- MetaHookSv requirement [Here](https://github.com/hzqst/MetaHookSv/blob/main/docs/Renderer.md#gpu-requirement)

### Installation Steps
1. Download MetaHookSv from [here](https://github.com/hzqst/MetaHookSv/releases). 
> [!CAUTION]
> For 3266 game build, use this specific version [here](https://github.com/hzqst/MetaHookSv/releases/tag/v20250225b). <ins>Choose blob.</ins> $\color{Red}{Important\ !}$

2. Copy `cstrike_hd`, `echoes`, `gearbox`, `platform`, `Metahook_blob.exe`, `SDL2.dll`, and `SDL3.dll` into your installed CS1.6 folder.
3. Open `svencoop` folder and copy everything into `cstrike` folder.
4. Back to your installed CS1.6 folder, rename the original `cstrike.exe` to something else if exist (as a backup).
5. Rename `Metahook_blob.exe` to `cstrike.exe`
6. Go to `cstrike\metahook\configs` folder, delete `plugins_svencoop.lst` and rename `plugins_goldsrc.lst` to `plugins.lst`.
