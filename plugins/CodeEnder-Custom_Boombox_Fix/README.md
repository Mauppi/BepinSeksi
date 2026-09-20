# CustomBoomboxFix
Workaround to allow music content mods to easily integrate with Custom Boombox Music.

## Usage
>(FOR ADVANCED USERS)

Creates `plugins/Custom Songs` directory and copies all folders inside `plugins` with name 'Custome Songs' into main custom boombox folder. Read decompiled code before use.

If you want to add some songs for personal use, just add the `.mp3` / `.wav` / `.ogg` files to `BepInEx/plugins/Custom Songs`. \
THIS WILL NOT SHARE WITH YOUR FRIENDS. If you want to share music with your friends, you either need to make a content mod or enable the share feature in the mod's configs. \
**You need permission from the creator to upload their music onto Thunderstore or to share music with friends! \
Do NOT just violate copyright.**

To create your own content mod, follow the guide [How to Create an Asset Replacement Mod](https://thunderstore.io/c/lethal-company/p/CodeEnder/Custom_Boombox_Fix/wiki/1396-how-to-create-an-asset-replacement-mod/).

To learn more about "share songs via configs", please read the guide [Sharing Music via Configs](https://thunderstore.io/c/lethal-company/p/CodeEnder/Custom_Boombox_Fix/wiki/2112-sharing-music-via-configs/).

Enabling the "share feature" will create a new `configs/Custom Songs` directory where you can put your music. The mod will handle the songs/folders in this directory the same way as the ones in the plugin directory. If you use this feature, simply sharing your Thunderstore profile code/file will now share the music you put in there too! \
**WARNING:** _Sharing songs via **profile code has a size limit of 20MB!** If you plan on using a lot of songs that way, you'll have to share your profile file!_


**CLIENT SIDE MOD.** Everyone needs to have it and the same music installed if you want everyone to listen to the same music. \
To fix music not being synced you can add mods like FutureSavior's [Boombox Sync Fix](https://thunderstore.io/c/lethal-company/p/FutureSavior/Boombox_Sync_Fix/).

## FAQ
#### I can't hear the music
Your files might not work, verify that they actually play music before installing them.
#### It's only playing the default songs
You likely didn't put the songs in the right folder. If you encounter this issue making a content mod, verify that your .zip file structure looks like this:
![](https://i.imgur.com/ac92pDe.png)

If you use **personal music**, you might have selected the wrong config and put your music in the wrong place
  - useStandardMethod = music should be in `plugins/Custom Songs` (also here if you haven't changed any configs)
  - useConfigShareMethod = music should be in `configs/Custom Songs`

#### Where did the default songs go?
If you want to bring the default songs back, you'll have to go into the config of the parent mod [Custom Boombox Music](https://thunderstore.io/c/lethal-company/p/Steven/Custom_Boombox_Music/).
#### My friends can't hear the music
They need this mod installed too, as well as your content mod.
#### My friends all hear different songs
Due to how Custom Boombox Music works, everyone needs to have the exact same songs installed for the boombox to be synced. \
However, if this is the case and there are still problems, you can add mods like FutureSavior's [Boombox Sync Fix](https://thunderstore.io/c/lethal-company/p/FutureSavior/Boombox_Sync_Fix/) to fix the issue.

## Support
This mod has been verified to be working correctly. Questions that can be answered by reading the available material will be ignored. If you still think you have a question, contact me on discord.

## Credits
Mod created by CodeEnder. \
v1.2.5 by [Inoyu](https://thunderstore.io/c/lethal-company/p/Inoyu/).

[Custom Boombox Music](https://thunderstore.io/c/lethal-company/p/Steven/Custom_Boombox_Music/) created by Steven.
