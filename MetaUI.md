# MetaUI Usage Tutorials
## This doc contains tutorials of using MetaUI.

> [!NOTE]
> [About MetaUI](https://github.com/asdian/CS1.6-Tutorials/blob/main/Chapter%20I%20-%20B.md#colorprocessbluemetaui-beta)

### $\color{BlueGreen}{A.\ Dynamic\ Hand\ Texture}$
In this tutorial, we will use Hyeonrin (buffclass25s5ct) as an example.

#### 1. Find the hand texture
CSO uses external texture files for their hand textures using targa files (.tga), in 512x512 dimension and 8-bit indexed color range. They uses a slight different hand texture system between males and females. For females, they're divided into 2 parts:
- `<handtexture_name>_femalelong.tga`
- `<handtexture_name>_femaleshort.tga`

For males, they're divided into 3 parts:
- `<handtexture_name>_malelong.tga`
- `<handtexture_name>_maleshort.tga`
- `<handtexture_name>_maleorg.tga`

Custom hand textures are usually stored in `(cstrike, dstrike, estrike, fstrike, common -if from .pak files-)/gfx/tattoo` directory.

![Hand texture files.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/hand_types.png)

For Hyeonrin, her hand textures are:
- `buffclass25s5ct_femalelong.tga`
- `buffclass25s5ct_femaleshort.tga`

<p align="center">
  <img src="https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/hyeonrin_F_L.png" width="40%" />
  <img src="https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/hyeonrin_F_S.png" width="40%" /> 
</p>

My MetaUI uses similar directory structure to find the hand textures: `cstrike/gfx/tattoo/`. Paste the hand textures there.

#### 2. Prepare the v_model files
Next, you need to prepare your custom v_models. Minimum requirements for your custom v_models are described below.
> [!NOTE]
> If you're using the raw files from CSO you should be good, no need to follow this section.

1. Make sure your custom v_model has `bodygroup`, under `hands` studio model name, and contains two hand model bodies. One male and one female.
![Hand bodygroup example.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/hand_bodygroup.png)

2. Determine the hand types as you need. Please note that you have to be consistent with the hand types. If the male uses `malelong`, then the female must use `femalelong` as well. For `maleorg` it's optional, but for female counterparts use `femaleshort`*.

*I might be wrong, if so please let me know.
