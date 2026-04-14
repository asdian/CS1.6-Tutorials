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

> [!TIP]
> If you want a quick test, replace all the original v_models in `models/` directory with my [custom v_models pack](https://www.mediafire.com/file/xoelvdek62pdewc/new_vmodels.rar/file) to see how it works. If replacing models doesn't work for some reason, create and use an AMX Mod X plugin or use external files method as described in [Resource Replacer](https://github.com/hzqst/MetaHookSv/blob/main/docs/ResourceReplacer.md) (we're mandatory to use MetaHookSv anyways).

### $\color{BlueGreen}{B.\ Custom\ Weapon\ HUD\ Image}$
Image demo: 

![Weapon HUD image demo.](https://github.com/asdian/CS1.6-Tutorials/blob/main/Pics/MetaUI/weapon_HUD.png)

The next feature is custom weapon HUD image. It means that you can set a custom weapon HUD image for each weapon just similar to CSO. Below is how to use it:

1. Make sure you have complete AMX Mod X installed.
2. Lookup at `metaui.inc`.

```txt
// ============================================================
// # Function: Register a custom weapon override on a client.
//             Tells MetaUI to load sprites/weapon_<txt_name>.txt
//             instead of the vanilla CS weapon txt when this weapon
//             is active, and to use the supplied max values as the
//             bar-fill denominators.
//
// # Param(s): (5)
//   id         : target player slot (1-32)
//   base_csw   : base CS weapon ID being substituted (e.g. CSW_DEAGLE)
//   txt_name   : bare weapon name, e.g. "desperado"
//                (client loads sprites/weapon_desperado.txt)
//   max_clip   : clip capacity for the ammo bar fraction denominator
//   max_bpammo : backpack ammo capacity for the bpammo bar fraction
// ============================================================
native metaui_set_custom_weapon(id, base_csw, const txt_name[], max_clip, max_bpammo)
```

3. Use that function inside weapon deploy hook. For example:

```txt

public Ham_CWeapon_Deploy_Post(iWpn) 
{
	if (is_nullent(iWpn) || !Had_Weapon(iWpn, WEAPON_CODE))
		return;

	static id; id = get_member(iWpn, m_pPlayer);

    set_entvar(id, var_viewmodel, V_CHAINMG);
    set_entvar(id, var_weaponmodel, P_CHAINMG);

    Stock_SendWeaponAnim(id, iWpn, 1);
	
	// Register the custom weapon override on the client.
	metaui_set_custom_weapon(id, CSW_CHAINMG, "chainmg", g_config_clip, g_config_bpammo)

	//.. other codes
}
```

4. Prepare the weapon HUD image files. They should be in `sprites/` directory and named as `weapon_<txt_name>.txt`. For example, if you're using `chainmg` as the `txt_name`, then the file should be named as `weapon_chainmg.txt`. The content of the file should be like this:

```txt
5
weapon		640	640hud241	0	90	170	45
weapon_s		640	640hud241	0	135	170	45
ammo		640   640hud7	72	72	24	24
ammo2		640	640hud224	49	231	24	24
kill			640 	640hud241	172	16	48	16
```

5. Also make sure the listed files are exists. In this case, they are: `640hud241.spr`, `640hud7.spr`, and `640hud224.spr`. If not, you should prepare them first.

6. MetaUI also will automatically registers the weapon kill hud icon from the `kill` entry above. You don't need to register it manually to the `sprites/hud.txt`.

7. That should be it. The weapon HUD image should be applied dynamically to your weapon when you're using it.