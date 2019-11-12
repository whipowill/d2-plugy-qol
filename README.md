# Diablo II QOL Mod Pack

This is a mod pack for Diablo II that brings together the best quality-of-life features I have found to maximize the singleplayer experience.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/F2wfSek.jpg)

## What's Included

- [PlugY](http://plugy.free.fr/en/index.html) - adds shared stash, infinite respec, all runewords.
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) - removes singleplayer FPS cap, adds auto gold pickup.
- [LinearMF](https://d2mods.info/forum/viewtopic.php?t=65492&start=200) - removes diminishing returns on magic find %.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) - makes 5s look like 5s instead of 6s.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) - skip the intro videos when you boot the game.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) - keep your equipment when you die.
- [LootFilter](https://pathofdiablo.com/) - adds the loot filter from Path of Diablo.
- [MultiRes](https://www.reddit.com/r/slashdiablo/comments/7z5uy1/hd_mod_and_maphack_new_release/) - adds widescreen resolutions to the game.

### Additional Changes

- Druid
    - Shapeshifting duration increased 50%.
    - Can summon all beasts at same time.

- Stack sizes increased (keys 24, scrolls 48).

## How To Install

- Purchase [registration keys](https://us.shop.battle.net/en-us/family/diablo-ii) from Blizzard.
- Install [Diablo II LOD](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) v1.12 (use this installer, don't downgrade v1.14).
- Install [Patch](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) v1.13d.
- Install [Glide](http://www.svenswrapper.de/english/files.html) v1.4e.
- Install [PlugY](http://plugy.free.fr/en/index.html) v11.02.
- Modify the properties of ``C:/Games/Diablo II/Mod PlugY/PlugY.exe`` to run as administrator and as Windows XP SP3.
- Modify the PlugY shortcut to have ``"C:/Games/Diablo II/Mod PlugY/PlugY.exe" -3dfx -direct -txt`` as the target.
- Download this [zipfile](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and paste into your D2 folder (one at a time, don't mass merge).
- Download files [#1](https://d2.lc/pod.dll) and [#2](https://d2.lc/D2PoDClient.dll) and paste into your D2 folder.
- Play the game.

If you're having errors and the install process didn't work for you, it's probably:

- You aren't using v1.13d.
- You tried to downgrade from v1.14, which you can't do.
- You didn't merge the files properly.

### How To Limited Install

If you want to install these mods but you don't want any changes to the actual gameplay (no changes to drops or skills), then delete the ``C:/Games/Diablo II/Mod PlugY/Data/Global/`` folder.

### How To Uninstall

Delete all the files you merged through this install process and copy the files from ``_backups`` and into your ``C:/Games/Diablo II/`` folder.

## Mac OSX

You can successfully install the game on Mac but you will have to use Wine in order to do it.  It's more advanced and requires the use of Terminal.  The best tutorial for doing this can be found [here](https://gist.github.com/whipowill/8f9a117895f2927cd6b52ccc611c8266).

## Keyboard Macros

This game is very clicky and you can quickly develop carpal tunnel syndrome by playing it.  To avoid this, I wrote a keyboard macro that lets you hold down the spacebar to move and attack.

- On PC using [AutoHotKey](https://autohotkey.com/), run this [script](https://raw.githubusercontent.com/whipowill/d2-plugy-qol/master/_macros/AutoAttack.ahk).
- On Mac using [Keyboard Maestro](https://www.keyboardmaestro.com/main/), run this [script](https://raw.githubusercontent.com/whipowill/d2-plugy-qol/master/_macros/AutoAttack.kmmacros).

After importing the macros on Mac, you'll need to specify that the macro is only for use in Wine.  Also note that you won't be able to type spaces while these scripts are running, but typing ``/players8`` still works w/ no space.

This makes melee characters a lot easier to play.

## Advanced Notes

- Make sure you don't have the [CPU fix](http://europebattle.net/d2/tools) installed, as BaseMod already has it.
- When you first select a widescreen resolution the game will crash, but only the first time.
- When you first boot the game you will have to click settings to activate the custom loot filter.
- The loot filter sometimes throws "invalid stat" errors in chat, but I don't think it breaks anything.
- There is a [StashMod](https://www.moddb.com/games/diablo-2-lod/addons/10x10-stash-mod-lod-113d-compatible) that increases inventory size, but I didn't include it in this pack.
- You can hold ``CONTROL`` and left-click items between inventory and stash (HT ubeogesh).

## Helpful Links

- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - Official guide to playing the game.
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - Keep track of your items as you find them.
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - See what runewords you can make.
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - A fan website w/ helpful information about the game.
- [Reddit Community](https://www.reddit.com/r/diablo2/) - A Reddit forum for the fans of D2.
- [Bugs List](https://us.battle.net/forums/en/d3/topic/6037267083) - A list of all the bugs in the game.

Be sure to also checkout my advice on how to properly [organize](https://github.com/whipowill/d2-plugy-qol/blob/master/STASH.md) your PlugY stash.

## Credits

- [PlugY](http://plugy.free.fr/en/index.html) by Yohann Nicolas.
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) by devurandom.
- [LinearMF](https://d2mods.info/forum/viewtopic.php?t=65492&start=200) by devurandom.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) by SnakeByteStudios.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) by SnakeByteStudios.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) by SnakeByteStudios.
- [LootFilter](https://pathofdiablo.com/) by Path of Diablo.
- [MultiRes](https://www.reddit.com/r/slashdiablo/comments/7z5uy1/hd_mod_and_maphack_new_release/) by SlashDiablo.