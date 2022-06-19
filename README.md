# SheepOS XFCE 64bit - Distro for the Render Farm Client

## Overview

SheepOS is a very lightweight Distro based on Porteus / Slackware for the free and distributed render farm [SheepIt](https://www.sheepit-renderfarm.com).

### Versions

This is the XFCE version, you can find the CLI version [here](https://github.com/zocker-160/SheepitOS/tree/CLI).

## Usage

 - Download the ISO and extract it (e.g. with Ark or 7zip) to a FAT32 formatted USB drive.
 - Boot from it
 - enjoy xD
 
### System requirements

 - min. 2GB RAM, the more the better ;)

## Building the ISO

Note: As far as I know, this method make's an image that only works for virtual machines.

1. Go the boot media.

![image](https://user-images.githubusercontent.com/50217071/174489933-546deac9-967c-4eb3-b6cc-0f41052f122a.png)

2. Go to the _porteus_ folder.

![image](https://user-images.githubusercontent.com/50217071/174489993-ad5dec55-23e6-47ca-8695-3857ceaa26cc.png)

3. There should be a _make_iso.sh_ file. Right click, then click, _Open terminal here_.

![image](https://user-images.githubusercontent.com/50217071/174490067-4044389a-3fd7-400a-af4b-bbcb014e2d1a.png)

4. Type, `sh make_iso.sh`.

5. Type the location, the name, and extension of the image.
Example: `/dev/sdb/images/ImageName.iso`

## Make auto-login on start
This one is a bit more complicated, but doable.
Also, watch out on the allowed maximum RAM usage.

1. Go the boot media.

![image](https://user-images.githubusercontent.com/50217071/174489933-546deac9-967c-4eb3-b6cc-0f41052f122a.png)

2. Go to the _porteus_ folder.

![image](https://user-images.githubusercontent.com/50217071/174489993-ad5dec55-23e6-47ca-8695-3857ceaa26cc.png)

3. Go to the _base_.

![image](https://user-images.githubusercontent.com/50217071/174490400-19d69baf-6a8d-4757-abf6-e9ee2d6eac97.png)

4. Right click on the SheepIt module, and extract it.

![image](https://user-images.githubusercontent.com/50217071/174490539-2d352681-46a1-4447-834b-4b70b8c9d42c.png)

5. Delete the .xzm module, so that we can free up a bit of space.

6. Change the settings, that you can see hidden files and folders, by pressing Ctrl + H

7. Go to the extracted module (_sheepit-module-xfce_), then _home_, and finally _guest_.

![image](https://user-images.githubusercontent.com/50217071/174490623-dcde8ac0-e1de-4c49-994f-c6f02b69a58f.png)

8. Open `.sheepit.conf`.

9. Edit the line number 2 from `false` to `true`.

![image](https://user-images.githubusercontent.com/50217071/174491018-93a5edbb-2df9-41f8-ae1a-e3bf47d93146.png)

10. Save and close the text editor.

11. Now, open `SheepItClient.sh`.

12. Edit the 4th line with your username and password/renderkey.

![image](https://user-images.githubusercontent.com/50217071/174492300-f1d57903-a3ea-4fa6-a36d-528a3c8bc352.png)


13. Save and close the text editor.

14. Head back to the `base` folder.

13. Right click on the SheepIt module folder, and then `Create xzm module`.

![image](https://user-images.githubusercontent.com/50217071/174491144-7fbb8907-e210-4083-a212-7611e66cce02.png)

13.1. (Optional) Delete the module **folder**.

14. Reboot!

## Adding own modules (e.g. nvidia-drivers)

//TODO

## Notes

- This distro supports only CPU rendering for now.
- If you use the *copy2RAM* option, you can unplug the boot media after the distro had booted. But it comes at the price of highr RAM usage.

## Issues/ToDo

[ ] Make that you simply need to burn the ISO, instead of extracting it.
