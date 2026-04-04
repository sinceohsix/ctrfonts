<div align=center>
  <img src="./titlebar.png">
</div>

---
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
5. [Special Thanks](#special-thanks)

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
| ![Preview](./fonts/screenshots/splat.jpg?raw=true) | ![Preview](./fonts/screenshots/zelda.jpg?raw=true) | ![Preview](./fonts/screenshots/undertale.jpg?raw=true) |

If you are curious about the custom HOME Menu layout in the screenshots above, you can download it from [here](https://aromakitsune.github.io/3DS-Custom-Home-Menu-UI). (Created by AromaKitsune)

## Converting Your Own Fonts
You can convert any compatible font file to an installable `SystemFont.cia` in as little as ~50 seconds. You have two ways of doing so, GitHub Actions or a Powershell script. GitHub Actions works on any device from a web browser but requires a GitHub account and a direct URL to a font. The Powershell script only requires a Windows machine and lets you convert any font you have (`.otf`, `.ttf`, or installed fonts). 

Both methods are based on the guide written by AromaKitsune and use the same tools and scripts. None of the tools used are made by me, you can find more info about them below.

>[!IMPORTANT]
>Neither of these guides are done yet, they are just placeholders.

### GitHub Actions
1. Fork this repository.
2. Go to actions
3. Enable workflows
4. Select 'ctrfont2' then run workflow
5. Enter a font url and run workflow

### Powershell
1. Clone this repository and extract the .zip
2. Run: `script.ps1 -FontFile [Path-to-otf/ttf file]`
3. Wait patiently.

## Tools Used
- [FontForge](https://fontforge.org/en-US/)
- CTR Font Converter
- [FontTool](https://github.com/astronautlevel2/FontTool) by astronautlevel2 & ihaveamac
- [3dstool](https://github.com/dnasdw/3dstool) by dnasdw and contributors
- [CTR_Toolkit](https://github.com/Tiger21820/ctr_toolkit) by Tiger21820 & 3DSGuy
- [`merge_fonts.py`](https://github.com/dkosmari/System-Font-Replacer/blob/main/merge-fonts.py) by dkosmari

### Special Thanks
First and foremost, this repository would not exist without the hard work of [AromaKitsune](https://github.com/aromakitsune). Huge shoutout to them for making their original guide on how to make custom fonts (found [here](https://aromakitsune.github.io/3DS-System-Font-Customization)) which was used as the basis to make the workflow.

I'd also like to give thanks to OctoRuler, a member of the [Custom 3DS Assets](https://discord.gg/0z7IGZ5Sv3D0mEN0) Discord server, for cheering me on and helping with the compatibility list.
