# Diablo II QOL Mod Pack

This is a mod pack for Diablo II that brings together the best quality-of-life features I have found to maximize the singleplayer experience.  Join our [Discord](https://discord.gg/KjDU67x) server for a community of D2QOL players.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/D1CKhA2.jpg)

## What's Included

- [PlugY](http://plugy.free.fr/en/index.html) - adds shared stash, infinite respec, all runewords.
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) - removes singleplayer FPS cap, adds auto gold pickup.
- [LinearMF](https://d2mods.info/forum/viewtopic.php?t=65492) - removes diminishing returns on magic find.
- [MercEquip](https://d2mods.info/forum/viewtopic.php?t=65492) - adds all equipment slots to mercenaries.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) - makes 5s look like 5s instead of 6s.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) - skip the intro videos when you boot the game.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) - keep your equipment when you die.
- [MapHack](https://github.com/youbetterdont/bhconfig/wiki/User-Guide) - shows the entire map w/ monsters and chests.
- [LootFilter](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) - filters items and get notified about drops.
- [MultiRes](https://www.reddit.com/r/slashdiablo/comments/7z5uy1/hd_mod_and_maphack_new_release/) - adds widescreen resolutions to the game.
- [DDraw](https://github.com/CnCNet/cnc-ddraw/releases) - improves video framerate, upscales graphics.

### Custom Changes

- Stacks
	- Keys stack to 24
	- Scrolls stack to 48
	- Quivers stack to 480

- Druid
	- Shapeshifting duration increased
	- Can summon all beasts at same time

- Quivers
	- Magic and rare quivers are possible
	- Arrows and bolts are infinite

- Corruption
	- Orb of Corruption - add sockets to a unique or set item
	- Orb of Transmutation - reforge a unique item to/from being Ethereal

- Mercenaries
	- Act 1 - Blessed Aim
	- Act 3 - Meditation
	- Act 5 - Might

- Misc
	- Countess always drops 3 runes
	- Rune upgrades no longer require gems
	- Deckard Cain relocated in Act 5 town

## How To Install

Backup your save files if you're upgrading an existing setup!

- Purchase keys from [Blizzard](https://us.shop.battle.net/en-us/family/diablo-ii).
- Install [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) - ``v1.12``
- Install [Patch](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) - ``v1.13d``
- Download this [zipfile](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and merge the files into your D2 install directory.
- Consult this [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Video.md) to configure your video settings.
- Modify the properties of ``C:/Games/Diablo II/Mod PlugY/PlugY.exe`` to run as admin and as Windows XP.
- Make a ``PlugY.exe`` shortcut on your desktop w/ a modified target:
	- If using ``DDraw`` - ``"C:/Games/Diablo II/Mod PlugY/PlugY.exe" -direct -txt``
	- If using ``Glide`` - ``"C:/Games/Diablo II/Mod PlugY/PlugY.exe" -w -3dfx -nofixaspect -direct -txt``
- Launch the game by running the ``PlugY`` shortcut you made.
- Modify the loot filter settings by clicking the ``BH`` button ingame.

If you're having errors and the install process didn't work for you, it's probably:

- You aren't using ``v1.13d``.
- You tried to downgrade from ``v1.14``, which you can't do.
- You didn't make the necessary [video](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Video.md) settings changes.
- You're missing the ``StormLib.dll`` file.
- You didn't merge the files properly.

### How To Install w/out Game Changes

If you want to install these mods but you don't want any changes to the actual gameplay (none of the custom game changes):

- Delete the ``C:/Games/Diablo II/Mod PlugY/Data/Global/`` folder.
- Turn ``MercEquip`` off in the ``BaseMod.ini`` file.

### How To Install On Mac OSX

You can successfully install the game on Mac but you will have to use Wine in order to do it.  It's more advanced and requires the use of Terminal.  I've written a [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/MacOSX.md) on how to do this.

### How To Uninstall

Delete all the files you merged through this install process and copy the files from ``Backups`` into your ``C:/Games/Diablo II/`` folder.

## Advanced Notes

- When you first select a widescreen resolution the game will crash, but only the first time.
- You can ``control-leftclick`` items between inventory and stash (HT ubeogesh).

### How To Use The Loot Filter

I wanted to keep the loot filter as simple as possible, and using the ingame panel you can set the ping to ``Tier 6`` and set the filter to your desired level:

- ``Off``
- ``Minimal`` - filters white items (lesser potions + most whites).
- ``Moderate`` - filters white and blue items (lesser potions + most whites/blues).
- ``Aggressive`` - filters white, blue, and rare items (lesser potions + most whites/blues/rares).

No matter what setting you use: runes, charms, jewels, gems, set items, unique items, special rare items, craftable magic items, and eligable white items are never filtered out.

You can inspect the ``BH.cfg`` config file to see exactly what is filtered out by searching the string ``FILTLVL``.  If I screwed up anything in this loot filter just open a ticket and let me know where I went wrong.

### How To Use The Keyboard Macros

This game is very clicky and you can quickly develop carpal tunnel syndrome by playing it.

To avoid this I wrote a [keyboard macro](https://github.com/whipowill/ahk-autoattack) that lets you hold down ``spacebar`` to move and attack (for PC and Mac).  This makes melee characters a lot easier to play.

## Helpful Links

- [Discord](https://discord.gg/KjDU67x) - Community and helpdesk for D2QOL players.
- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - Official guide to playing the game.
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - Keep track of your items as you find them.
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - See what runewords you can make.
- [D1RU's Skill Calculator](http://www.diablo1.ru/poleznoe/calculator.php) - Plan your skill allocations.
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - Fan website w/ helpful information about the game.
- [Reddit](https://www.reddit.com/r/diablo2/) - Online forum for all the D2 fans.
- [Arq](https://www.arqbackup.com/) - App for backing up your save files.

## Credits

- [PlugY](http://plugy.free.fr/en/index.html) by Yohann Nicolas.
- [BaseMod](https://d2mods.info/forum/viewtopic.php?t=65492) by devurandom.
- [LinearMF](https://d2mods.info/forum/viewtopic.php?t=65492) by devurandom.
- [MercEquip](https://d2mods.info/forum/viewtopic.php?t=65492) by devurandom.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) by SnakeByteStudios.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) by SnakeByteStudios.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) by SnakeByteStudios.
- [MapHack](https://github.com/youbetterdont/slashdiablo-maphack) by SlashDiablo.
- [LootFilter](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) by SlashDiablo.
- [MultiRes](https://www.reddit.com/r/slashdiablo/comments/7z5uy1/hd_mod_and_maphack_new_release/) by SlashDiablo.
- [DDraw](https://github.com/CnCNet/cnc-ddraw/releases) - by CnCNet.

## Changelog

- ``2020-09-24`` - Update BaseMod to ``1.3.3``.
- ``2020-09-22`` - Add corruption mechanic.
- ``2020-09-14`` - Make ``PlugY``, ``Glide``, and ``DDraw`` preinstalled.
- ``2020-09-01`` - Replace loot filter.
- ``2019-11-01`` - Original release.