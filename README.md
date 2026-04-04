# ctrfonts

A repository with dozens of custom Nintendo 3DS system fonts to personalize your console! You can also convert your own fonts using GitHub Actions (based on the [guide by AromaKitsune](https://aromakitsune.github.io/3DS-System-Font-Customization)).

Custom firmware (CFW) is required to install custom fonts. You can setup custom firmware with [this guide](https://3ds.hacks.guide).

>[!NOTE]
>Some games use the system font to display text in-game. In certain games this means your custom font will show up, and in others, the text may appear corrupted or not show up at all. A list of games that are affected can be found at [compatibility.md](./compatibility.md).

>[!CAUTION]
>Custom fonts are safe as long as you have Boot9Strap and GodMode9 installed. Uninstalling CFW while having a custom font installed will brick your console. **It is highly recommended that you make a NAND backup before modifying system files**.

## Contents
1. [Fonts](#fonts)
2. [Previews](#previews)
3. [Converting Your Own Fonts](#converting-your-own-fonts)
4. [Tools Used](#tools-used)

## Fonts
There are currently **4** fonts available.  
[Installing Custom Fonts](#installing-custom-fonts) · [Uninstalling Custom Fonts](#uninstalling-custom-fonts)

| Preview | Font | Download |
| :-----: | :--: | :------: |
| ![Font](/fonts/previews/FOT-PopHappiness-Std-EB.png) | Pop Happiness | [Download](https://github.com/sinceohsix/ctrfonts/releases/download/FOT-PopHappiness-Std-EB/SystemFont.cia) |
| ![Font](/fonts/previews/MARIO-MAKER.png) | MARIO MAKER | [Download](https://github.com/sinceohsix/ctrfonts/releases/download/MARIO-MAKER/SystemFont.cia) |
| ![Font](/fonts/previews/Zelda-Glyphs-v2-Deco.png) | Zelda Glyphs | [Download](https://github.com/sinceohsix/ctrfonts/releases/download/Zelda-Glyphs-v2-Deco/SystemFont.cia) |
| ![Font](/fonts/previews/Determination-Sans.png) | DETERMINATION Sans | [Download](https://github.com/sinceohsix/ctrfonts/releases/download/Determination-Sans/SystemFont.cia) |


### Installing Custom Fonts

>[!IMPORTANT]
>Installing custom system fonts with FBI is not recommended. Use GodMode9 by following the steps below.

1. Download `SytemFont.cia` file and transfer it to your 3DS' (micro)SD Card via FTP or an SD Card reader.
2. Hold `Start` while powering on your 3DS. Select GodMode9 if prompted.
3. Select the `[0:] SDCARD (***)` directory.
4. Navigate to where you saved your `SystemFont.cia` file, then select it.
5. Select `CIA image options...` then `Install game image`.
6. Press `A` to unlock SysNAND then follow the prompts. Press `A` after the font is installed, then press it again.
7. Press `Start` to reboot to the HOME Menu.

Your custom font should be applied. If you get a crash/error message instead, this means your font is not compatible and you will need to [restore the default system font](#uninstalling-custom-fonts).

### Uninstalling Custom Fonts 

1. Download the original [`SystemFont.cia`]()
2. Transfer the file to your 3DS' (micro)SD Card via FTP or an SD Card reader.
3. Hold `Start` while powering on your 3DS. Select GodMode9 if prompted.
4. Select the `[0:] SDCARD (***)` directory.
5. Navigate to where you saved the orignal `SystemFont.cia` file, then select it.
6. Select `CIA image options...` then `Install game image`.
7. Press `A` to unlock SysNAND then follow the prompts. Press `A` after the font is installed, then press it again.
8. Press `Start` to reboot to the HOME Menu.

The orignal system font has been restored. 

## Previews
Here are some previews of how you can style your 3DS with custom fonts! These screenshots were taken on a real 3DS console for accuracy.

Click or tap an image to see it in original quality.

|                       Splatoon                     |                The Legend of Zelda                 |                        Undertale                     |
| :------------------------------------------------: | :------------------------------------------------: | :--------------------------------------------------: |
| ![Preview](./fonts/screenshots/splat.jpg?raw=true) | ![Preview](./fonts/screenshots/zelda.jpg?raw=true) | ![Preview](./fonts/screenshots/undertale.jpg?raw=true)

## Converting Your Own Fonts
By using GitHub Actions, you can convert any compatible font file to an installable `SystemFont.cia` in as little as ~50 seconds! The workflow is based on the guide written by AromaKitsune and uses the same tools and scripts. None of the tools used are made by me, you can find more info about them below.

## Tools Used
- [FontForge](https://fontforge.org/en-US/)
- CTR Font Converter
- [FontTool](https://github.com/astronautlevel2/FontTool) by astronautlevel2 & ihaveamac
- [3dstool](https://github.com/dnasdw/3dstool) by dnasdw and contributors
- [CTR_Toolkit](https://github.com/Tiger21820/ctr_toolkit) by Tiger21820 & 3DSGuy
- [`merge_fonts.py`](https://github.com/dkosmari/System-Font-Replacer/blob/main/merge-fonts.py) by dkosmari
