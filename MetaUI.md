# MetaUI Usage Tutorials
## This doc contains tutorials of using MetaUI.

> [!NOTE]
> [About MetaUI](https://github.com/asdian/CS1.6-Tutorials/blob/main/Chapter%20I%20-%20B.md#colorprocessbluemetaui-beta)

### $\color{BlueGreen}{A.\ Dynamic\ Hand\ Texture}$
MetaUI has dynamic hand texture feature. It means that the available hand texture of the currently using player model will be applied to every supported v_model.

#### 1. Determine the hand texture
CSO uses external texture files for their hand textures using targa files (.tga), in 512x512 dimension and 8-bit indexed color range. They uses a slight different hand texture system between males and females. For females, they're divided into 2 parts:
- `<handtexture_name>_femalelong.tga`
- `<handtexture_name>_femaleshort.tga`

For males, they're divided into 3 parts:
- `<handtexture_name>_malelong.tga`
- `<handtexture_name>_maleshort.tga`
- `<handtexture_name>_maleorg.tga`

MetaUI is mimicking that system into regular CS1.6.

#### 2. Prepare the v_model files
Next, you need to prepare your custom v_models. Minimum requirements for your custom v_models are described below.
> [!NOTE]
> If you're using the raw files from CSO you should be good, no need to follow this section.

1. Make sure your custom v_model has `bodygroup` entry under `hands` studio name, and contains two hand model bodies, one male and one female. If it doesn't, modify the model first. (This guide is not about how to modify a v_model.)

![Hand bodygroup example.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/bodygroup.png)

2. Determine the hand types as you need. Please note that you have to be consistent with the hand types. If the male uses `malelong`, then the female must use `femalelong` as well. For `maleorg` it's optional, but for female counterparts use `femaleshort` (I might be wrong, if so please let me know).

3. Bind the texture files using one of these specific names:
- `#256256hand.bmp` 
- `#256252hand.bmp` 
- `#512512cso_highq_hand__long_512.bmp`
- `#512512cso_girl_hand.bmp`
- `#508506cso_girl_hand.bmp`
- `#512512cso_girl_hand_long.bmp`

4. Set the texture dimension inside the v_model to (4x1)

![Hand texture binding example.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/hand_texture.png)

5. That should be it. The hand texture should be applied dynamically to your v_model when you're using it.

### $\color{BlueGreen}{B.\ Custom\ Weapon\ HUD\ Image}$
Image demo: 

![Weapon HUD image demo.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/weapon_HUD.png)