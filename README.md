# Diablo II QOL Mod Pack

This is a mod pack for Diablo II v1.13d that brings together the best quality-of-life features I have found to maximize the singleplayer experience, with the goal of enhancing the game in a limited and tasteful way.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/F2wfSek.jpg)

## What's Included

- [PlugY](http://plugy.free.fr/en/index.html) - adds unlimited stash, shared stash, infinite respec, all runewords.
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) - removes singleplayer FPS cap, adds auto gold pickup.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) - makes 5s look like 5s instead of 6s.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) - skip the intro videos when you boot the game.
- [DropMod](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#betterdrops) - 2X as likely to find uniques, 1.5X to find sets, no change to runes.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) - keep your equipment when you die (I play HC so I don't care about this).
- [LootFilter](https://github.com/Synial/SynFilter/tree/cd4ab9d8b51320973c7b3df9c90b74b3d1ea8f91/xfiles) - adds the loot filter from [Path of Diablo](https://pathofdiablo.com/).
- [MultiRes](https://drive.google.com/drive/folders/1hLbrYs_U7eVcK-bWOom_Lr2_Y839AVba) - adds widescreen resolutions to the game.

### Additional Changes

- Druid
    - Shapeshifting duration increased 50%.
    - Can summon all beasts at same time.

## How To Install

- Purchase [registration keys](https://us.shop.battle.net/en-us/family/diablo-ii).
- Install [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc).
- Install [Patch v1.13d](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe).
- Install [Glide](http://www.svenswrapper.de/english/files.html).
- Install [PlugY](http://plugy.free.fr/en/index.html).
- Modify the properties of ``PlugY.exe`` to run as administrator and as Windows XP (SP 3).
- Modify the PlugY shortcut to have ``"...PlugY.exe" -3dfx -direct -txt`` as the target.
- Download this [zipfile](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and carefully merge the files into your D2 folder.

### How To Limited Install

If you want to install these mods but you don't want any changes to the actual gameplay (no changes to drops or skills), then delete the ``Mod PlugY/data/global/`` folder.

### How To Uninstall

Delete all the files you merged through this install process and copy the files from ``_backups`` and paste them into your ``C:\your\path\to\Diablo II\`` folder.

## Mac OSX

You can successfully install the game on Mac but you will have to use Wine in order to do it.  It's more advanced and requires the use of Terminal.  The best tutorial for doing this can be found [here](https://gist.github.com/whipowill/8f9a117895f2927cd6b52ccc611c8266).

## Keyboard Macros

This game is very clicky and you can quickly develop carpal tunnel syndrome by playing it.  To avoid this, I wrote a keyboard macro that lets you hold down the spacebar to simulate repeated mouse clicks.

- On PC using [AutoHotKey](https://autohotkey.com/), run this [script](https://raw.githubusercontent.com/whipowill/d2-plugy-qol/master/_macros/AutoAttack.ahk).
- On Mac using [Keyboard Maestro](https://www.keyboardmaestro.com/main/), run this [script](https://raw.githubusercontent.com/whipowill/d2-plugy-qol/master/_macros/AutoAttack.kmmacros).

After importing the macros on Mac, you'll need to specify that the macro is only for use in Wine.  Also note that you won't be able to type spaces while these scripts are running, but typing ``/players8`` still works w/ no space.

This makes melee characters a lot easier to play.

## Advanced Notes

- Make sure you don't have the [CPU fix](http://europebattle.net/d2/tools) installed, as BaseMod already has it.
- When you first select a widescreen resolution the game will crash, but only the first time.
- When you first boot the game you will have to click settings to activate the custom loot filter.
- The loot filter sometimes throws "invalid stat" errors in chat, but I don't think it breaks anything.
- There is a [StashMod](https://www.moddb.com/games/diablo-2-lod/addons/10x10-stash-mod-lod-113d-compatible) which increases inventory size, but I didn't include it in this pack.
- I wish I could shift-click between inventory and stash.

## Helpful Links

- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - Official guide to playing the game.
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - Keep track of your items as you find them.
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - See what runewords you can make.
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - A fan website w/ helpful information about the game.
- [Reddit Community](https://www.reddit.com/r/diablo2/) - A Reddit forum for the fans of D2.
- [Bugs List](https://us.battle.net/forums/en/d3/topic/6037267083) - A list of all the bugs in the game.

Be sure to also checkout my advice on how to properly [organize](https://github.com/whipowill/d2-plugy-qol/blob/master/STASH.md) your PlugY stash.

## Credits

- [PlugY](http://plugy.free.fr/en/index.html) provided by [Yohann Nicolas](http://plugy.free.fr/en/index.html) (v11.02).
- [BaseMod](https://www.dropbox.com/s/fj3f5smvxdld3kx/BaseMod106.zip) provided by [devurandom](https://d2mods.info/forum/viewtopic.php?t=65492) (v1.06).
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) provided by [SnakeByteStudios](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/).
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) provided by [SnakeByteStudios](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/).
- [DropMod](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#betterdrops) provided by [SnakeByteStudios](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/).
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) provided by [SnakeByteStudios](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/).
- [LootFilter](https://github.com/Synial/SynFilter/tree/cd4ab9d8b51320973c7b3df9c90b74b3d1ea8f91/xfiles) provided by [Path of Diablo](https://pathofdiablo.com/).
- [MultiRes](https://drive.google.com/drive/folders/1hLbrYs_U7eVcK-bWOom_Lr2_Y839AVba) provided by [SlashDiablo](https://www.reddit.com/r/slashdiablo/comments/7z5uy1/hd_mod_and_maphack_new_release/).