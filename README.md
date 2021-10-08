# Diablo II QOL Mod Pack

This is a mod pack for Diablo II that brings together the best quality-of-life features I have found to maximize the singleplayer experience.  Join our [Discord](https://discord.gg/KjDU67x) server for a community of D2QOL players.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/D1CKhA2.jpg)

## What's Included

- [PlugY](http://plugy.free.fr/en/index.html) - adds shared stash, infinite respec, all runewords (v14.02).
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) - adds auto gold pickup, bug fixes, and much much more (v1.13.7).
- [LinearMF](https://d2mods.info/forum/viewtopic.php?t=65492) - removes diminishing returns on magic find.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) - makes 5s look like 5s instead of 6s.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) - skip the intro videos when you boot the game.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) - keep your equipment when you die.
- [MapHack](https://github.com/youbetterdont/bhconfig/wiki/User-Guide) - shows the entire map w/ monsters and chests.
- [LootFilter](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) - filters items and get notified about drops.
- [D2DX](https://github.com/bolrog/d2dx/releases) - adds widescreen resolutions and wildly improves framerate (v0.99.529).
- [3DSound](https://www.indirectsound.com/downloads.html) - enables 3d sound option in sound settings.

### Custom Changes

- Druid
	- Shapeshifting duration increased
	- Can summon all beasts at same time

- Mercenaries
	- Act 1 - Blessed Aim
	- Act 3 - Meditation
	- Act 5 - Might

- Misc
	- Countess always drops 3 runes
	- Deckard Cain relocated in Act 5 town

## Install

- Purchase keys from [Blizzard](https://us.shop.battle.net/en-us/family/diablo-ii).
- Install [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) - ``v1.12``
- Install [Patch](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) - ``v1.13d``
- Download this [zipfile](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and merge the files into your D2 install directory.
- Consult this [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Video.md) to configure your video settings.
- Make a ``Game.exe`` shortcut on your desktop w/ modifications:
	- If using ``DDraw`` set target to ``"C:/Games/Diablo II/Game.exe" -direct -txt``.
	- If using ``Glide`` set target to ``"C:/Games/Diablo II/Game.exe" -3dfx -direct -txt``.
- Launch the game by running the shortcut you made.
- Modify the loot filter settings by clicking the ``BH`` button ingame.

### Game Changes

If you want to install these mods but you don't want any changes to the actual gameplay (none of the custom game changes) then delete the ``C:/Games/Diablo II/Data/Global/`` folder.

### Mac / Linux

You can successfully install the game on Mac and Linux but you will have to use Wine in order to do it.  It's more advanced and requires the use of Terminal.  I've written a [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Unix.md) on how to do this.

### Uninstall

Delete all the files you merged through this install process and copy the files from ``Backups`` into your ``C:/Games/Diablo II/`` folder.

## Advanced

- You can ``control-leftclick`` items between inventory and stash.

### Loot Filter

I wanted to keep the loot filter as simple as possible, and using the ingame panel you can set the ping to ``Tier 6`` and set the filter to your desired level:

- ``Off``
- ``Minimal`` - filters white items.
- ``Moderate`` - filters white and magic items.
- ``Aggressive`` - filters white, magic, and rare items.

No matter what setting you use: runes, charms, jewels, gems, rings, ammulets, set items, unique items, and eligable socketable items are never filtered out.

### Keyboard Macros

This game is very clicky and you can quickly develop carpal tunnel syndrome by playing it.  To avoid this I wrote a [keyboard macro](https://github.com/whipowill/ahk-autoattack) that lets you hold down ``spacebar`` to move and attack.  This makes melee characters a lot easier to play.

## Helpful Links

- [Discord](https://discord.gg/KjDU67x) - Community and helpdesk for D2QOL players.
- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - Official guide to playing the game.
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - Keep track of your items as you find them.
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - See what runewords you can make.
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - Fan website w/ helpful information about the game.
- [D2 Planner](https://d2planner.github.io/skills/?eyJ2IjoxLCJwIjoiMS4xNEQiLCJjIjoiYW1hem9uIiwicyI6e30sImIiOnt9LCJ0IjoxfQ==) - Plan your skill allocations.
- [Reddit](https://www.reddit.com/r/diablo2/) - Online forum for all the D2 fans.
- [Arq](https://www.arqbackup.com/) - App for backing up your save files.

## Credits

- [PlugY](http://plugy.free.fr/en/index.html) by Yohann Nicolas.
- [UberMod](https://github.com/Snapchip/D2UberMod) by snapchip.
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) by devurandom.
- [LinearMF](https://d2mods.info/forum/viewtopic.php?t=65492) by devurandom.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) by SnakeByteStudios.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) by SnakeByteStudios.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) by SnakeByteStudios.
- [MapHack](https://github.com/youbetterdont/slashdiablo-maphack) by SlashDiablo.
- [LootFilter](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) by SlashDiablo.
- [MultiRes](https://www.reddit.com/r/slashdiablo/comments/7z5uy1/hd_mod_and_maphack_new_release/) by SlashDiablo.
- [DDraw](https://github.com/CnCNet/cnc-ddraw/releases) - by CnCNet.
- [D2DX](https://github.com/bolrog/d2dx/releases) - by Bolrog.
- [3DSound](https://www.indirectsound.com/downloads.html) - by IndirectSound.