
# GBA icons for TwilightMenu++
This repository contains a pack of icons for Game Boy Advance games launched from TwilightMenu++.

These icons are taken from [libretro-thumbnails boxarts](https://github.com/libretro-thumbnails/Nintendo_-_Game_Boy_Advance/tree/master/Named_Boxarts).

They were all converted to [the proper format](https://github.com/DS-Homebrew/TWiLightMenu/pull/1800) with the following commands:

```
mkdir ./icons
for file in *.png; do
	convert "$file" -resize 32x32 -colors 15 -strip "./icons/${file%.png}.gba.png";
done
```

If you want to make a single icon from another boxart (e.g. for a homebrew game), you can use the following command:
```
convert original.png -resize 32x32 -colors 15 -strip gamename.gba.png
```

## Usage

Just download the icons you want and copy them to your SD card to the path `sd:/_nds/TWiLightMenu/icons`.

If you want to copy [all of them](https://github.com/Axce/twilightmenu-gba-icons/archive/refs/heads/main.zip), you can (the full size is only 3.4 Mo), but TwilightMenu++ loadings will take much longer.

if your gba games have the No-Intro file names, you have nothing more to do.

Otherwise, for an icon to appear, it should have exactly the same name as the game, ending with `.gba.png`. For example, `Wario Land 4 (USA, Europe).gba.png`.

