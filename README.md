# Diablo II QOL Mod Pack

This is a mod pack for Diablo II that brings together the best quality-of-life features I have found to maximize the singleplayer experience.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/D1CKhA2.jpg)

## Introduction

It's been 25 years and we're still playing this game.  Hats off to the [Project Diablo 2](http://projectdiablo2.com/) guys who continue to do amazing work, w/ modding capabilities second to none.  For those looking to revisit the vanilla experience, this modpack might be just what you wanted.

**This repo is just for tweaks to the game engine, adding QOL features w/ no changes to the game itself.**

### Other Projects

- [Reformed](https://github.com/whipowill/d2-mod-reformed) - My soft-mod (TXT files) changes to the game (both D2LOD and D2R).
- [Qolbot](https://github.com/whipowill/d2-qolbot) - Play multiplayer w/ your other singleplayer characters.

### HELP WANTED!

Act 1 mercs can't equip quivers and I don't have the skills to fix it (requires DLL work).  Also, I don't know how to make the hex edit that fixes merc running animation when out of combat in v1.13d (clue [here](https://d2mods.info/forum/viewtopic.php?t=63030)).

If anyone knows how to fix these issues, open a ticket and let's discuss!  I'd be so grateful.

## What's Included

- [D2GL](https://github.com/bayaraa/d2gl/releases/tag/v1.0.4) - Widescreen resolutions, HD upgrades, and wildly improves framerate (v1.0.4).
- [D2FPS](https://github.com/Jarcho/d2-rs) - Used in combo w/ D2GL and makes FPS even better, smooth as butter (v1.0.2).
- [PlugY](http://plugy.free.fr/en/index.html) - Adds infinite stash, shared stash, infinite respec, all runewords (v14.02).
- [BaseMod](https://www.moddb.com/mods/basemod) - Configurable settings, bug fixes, and much much more (v1.13.9).
- [AutoPickup](https://www.moddb.com/mods/basemod) - Automatically pickup gold, scrolls, keys, and arrows.
- [QuestRewards](https://www.moddb.com/mods/basemod) - Pay Akara/Charsi/Larzuk to respec/imbue/socket more than once.
- [UberMod](http://plugy.free.fr/en/index.html) - Take down Diablo Clone and the Uber bosses in singleplayer.
- [LinearMF](https://www.moddb.com/mods/basemod) - Removes diminishing returns on magic find.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) - Makes 5s look like 5s instead of 6s.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) - Skip the intro videos when you boot the game.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) - Keep your equipment when you die.
- [MapHack](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) - Shows the entire map w/ monsters and chests (BH v1.9.10).
- [LootFilter](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) - Filter items and get notified about important drops (BH v1.9.10).
- [BuffIcons](https://github.com/BeLikeLeBron/slashdiablo-maphack) - Shows your current buff and debuff icons (BH v1.9.10).
- [3DSound](https://www.indirectsound.com/downloads.html) - Enables 3D sound option in sound settings (Windows only).
- [ItemLabels](https://github.com/Trihedraf/d2-item-labels) - Toggle "always show items" on or off (v1.0.0).
- [D2RCinematics](https://www.moddb.com/downloads/cinematics-from-diablo-2-resurrected-for-diablo-2-lord-of-destruction) - Use the new cinematic cutscenes from D2R.
- [NoPenaltyMonsters](https://d2mods.info/forum/viewtopic.php?p=496186#p496186) - Remove XP penalty when you're higher level than monsters.
- **NoPenaltyParty** - Low lvl players still get XP when partied w/ high lvl players (hex edit by me).

## Install

### Windows

- Purchase keys from [Blizzard](https://us.shop.battle.net/en-us/family/diablo-ii).
- Install [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) - ``v1.12``
- Install [v1.13d patch](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) - ``v1.13d``
- Download [modpack files](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and merge the files into your D2 install directory.
- Download [cinematic files](https://www.moddb.com/downloads/start/222392) and place the contents in ``C:\Games\Diablo II\Data\local\video\eng\``.  I didn't include these files in this repo bc a) they are 500mb, and b) I don't want a copyright complaint.
- Make a ``Game.exe`` shortcut w/ target ``"C:\Games\Diablo II\Game.exe" -3dfx -direct -txt``.
- Launch the game by running the shortcut you made.

**Special Keybinds**

- Press ``0`` to show/hide the maphack settings button
- Press ``9`` to reload the maphack settings
- Press ``B`` to show the verbose stats screen
- Press ``L`` to show/hide items on the ground
- Press ``Control-O`` to open the graphics settings

If your maphack settings button will not show, try deleting the ``C:\Games\Diablo II\UI.ini`` file (if it exists) and reload the game.

### Mac/Linux

You can successfully install the game on Mac and Linux but you will have to use Wine in order to do it.  It's more advanced and requires the use of Terminal.  I've written a [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Unix.md) on how to do this.

**I recommend [Bottles](https://usebottles.com/) on Linux!**

### Uninstall

Delete all the files you merged through this install process and copy the files from ``Backups`` into your ``C:\Games\Diablo II\`` folder.

## Settings

Since this modpack includes a compilation of various mods, there are several places where you can tweak things:

- ``PlugY.ini`` - stash settings
- ``BaseMod.ini`` - game settings
- ``BH_settings.cfg`` - maphack settings
- ``BH.cfg`` - loot filter settings (check [documentation](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/))
- ``d2gl.ini`` - video settings
- ``d2fps.ini`` - video settings

## Keyboard

This game is very clicky and you can quickly develop carpal tunnel syndrome.  To avoid this I wrote an [AutoHotKey](https://github.com/whipowill/ahk-autoattack) script that lets you hold down ``spacebar`` to move and attack.  This makes melee characters a lot easier to play.

**I recommend this alternate [version](https://github.com/whipowill/sh-d2-autoattack) on Linux!**

## Hero Editor

One of the benefits of playing vanilla Diablo II is you can still make use of all the old tools.  When using [Hero Editor](https://www.moddb.com/games/diablo-2-lod/downloads/hero-editor-v-104), be sure to make the following changes to your ``config.ini`` file so it will still work w/ PlugY:

```
ErrorIgnore=1
LargerStashPicture=1
StashHeight=10
StashWidth=10
```

## External Links

- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - Official guide to playing the game.
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - Keep track of your items as you find them.
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - See what runewords you can make.
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - Fan website w/ helpful information about the game.
- [D2 Planner](https://d2planner.github.io/skills/) - Plan your skill allocations.
- [Reddit](https://www.reddit.com/r/diablo2/) - Online forum for all the D2 fans.
- [ProjectDiablo2](http://projectdiablo2.com/) - These guys are taking the game to a whole new level.
- [SlashDiablo](http://slashdiablo.net/) - If you want to play the original game online.
- [Loot Filter Rules](https://github.com/planqi/slashdiablo-maphack/wiki/Stats) - A list of the official loot filter coding rules.
- [Hero Editor](https://www.moddb.com/games/diablo-2-lod/downloads/hero-editor-v-104) - A Windows app for editing your character files.

## Credits

- D2GL by __Bayaraa__
- D2FPS by __Jarcho__
- PlugY by __Yohann Nicolas__
- UberMod by __SnapChip__
- BaseMod, AutoPickup, QuestRewards, LinearMF, NoPenaltyMonsters by __devurandom__
- FontFix, NoIntro, KeepEquip by __SnakeByteStudios__
- MapHack, LootFilter, BuffIcons by __SlashDiablo__
- 3DSound by __IndirectSound__
- ItemLabels by __Trihedraf__
- D2RCinematics by __N3UR0N3TW0RK__

Special thanks to all the fans of this amazing game for keeping it alive.