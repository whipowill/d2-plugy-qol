# Diablo II QOL Mod Pack

This is a mod pack for Diablo II that brings together the best quality-of-life features I have found to maximize the singleplayer experience.  Join our [Discord](https://discord.gg/KjDU67x) server for a community of D2QOL players.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/D1CKhA2.jpg)

## What's Included

- [D2GL](https://github.com/bayaraa/d2gl/releases/tag/v1.0.4) - widescreen resolutions, HD upgrades, and wildly improves framerate (v1.0.4).
- [PlugY](http://plugy.free.fr/en/index.html) - adds infinite stash, shared stash, infinite respec, all runewords (v14.02).
- [BaseMod](https://www.moddb.com/mods/basemod) - configurable settings, bug fixes, and much much more (v1.13.9).
- [AutoPickup](https://www.moddb.com/mods/basemod) - automatically pickup gold, scrolls, keys, and arrows.
- [QuestRewards](https://www.moddb.com/mods/basemod) - pay Akara/Charsi/Larzuk to respec/imbue/socket more than once.
- [UberMod](http://plugy.free.fr/en/index.html) - take down Diablo Clone and the Uber bosses in singleplayer.
- [LinearMF](https://www.moddb.com/mods/basemod) - removes diminishing returns on magic find.
- [NoPenalty](https://d2mods.info/forum/viewtopic.php?p=496186#p496186) - remove XP penalty when you're higher level than monsters.
- [FontFix](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#fixedfont) - makes 5s look like 5s instead of 6s.
- [NoIntro](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#nointro) - skip the intro videos when you boot the game.
- [KeepEquip](https://www.snakebytestudios.com/projects/mods/diablo-2-mods/#equipmentdeath) - keep your equipment when you die.
- [MapHack](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) - shows the entire map w/ monsters and chests.
- [LootFilter](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) - filter items and get notified about important drops.
- [3DSound](https://www.indirectsound.com/downloads.html) - enables 3D sound option in sound settings.

## Install

### Windows

- Purchase keys from [Blizzard](https://us.shop.battle.net/en-us/family/diablo-ii).
- Install [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) - ``v1.12``
- Install [Patch](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) - ``v1.13d``
- Download this [zipfile](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and merge the files into your D2 install directory.
- Make a ``Game.exe`` shortcut w/ target ``"C:\Games\Diablo II\Game.exe" -3dfx -direct -txt``.
- Launch the game by running the shortcut you made.
- Hold ``SHIFT`` and drag the ``BH`` icon to the bottom left corner.
- Hold ``CONTROL`` and click the ``BH`` button to bring up the maphack settings.

### Mac/Linux

You can successfully install the game on Mac and Linux but you will have to use Wine in order to do it.  It's more advanced and requires the use of Terminal.  I've written a [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Unix.md) on how to do this.

### Uninstall

Delete all the files you merged through this install process and copy the files from ``Backups`` into your ``C:\Games\Diablo II\`` folder.

## Settings

Out of the box, this modpack includes my settings.  These may not be the settings you prefer, but they are the settings I prefer, and here's why:

- I set 10 pages max in the shared stash.  Having infinite stash allows you to acquire infinite wealth, and infinite wealth strips you of the joy and excitement of finding new items.  Scarcity is a fundamental part of this game.

- I disable skill point unassignment, but I enable Akara to respec you more than once for a fee.  This makes the game feel more like a game and less like spreadsheet editing.  It's fun to save up for a big respec.

- I make all items drop as identified.  This saves me a ton of time as I can inspect an item from the ground w/out having to pick it up.  This lets me use the loot filter more aggressively.

Feel free to edit ``d2gl.ini``, ``PlugY.ini``, and ``BaseMod.ini`` to the settings you want to play.

## Soft Mods

Included in this [folder](https://github.com/whipowill/d2-plugy-qol/tree/master/Mods) are several "soft mods" that are popular in the D2 community which include changes to inventory, drops, mercenaries, skills, and more.

These mods are separated into individual folders so you can pick and choose what you want.  None of these mods are turned on by default in this modpack, you have to turn them on yourself.

To install any of these, just copy and paste the individual folder contents into ``C:\your\path\to\Diablo II\Data\Global\Excel\``.

## Loot Filter

You can edit the ``BH.cfg`` file to make your own loot filter rules, but I've included the one that I use.  For a deep dive into the inner-workings of the loot filter, checkout SlashDiablo's [release](https://www.reddit.com/r/slashdiablo/comments/hw0dro/announcing_slash_bh_199/) page.

## Keyboard Macros

This game is very clicky and you can quickly develop carpal tunnel syndrome.  To avoid this I wrote a [keyboard macro](https://github.com/whipowill/ahk-autoattack) that lets you hold down ``spacebar`` to move and attack.  This makes melee characters a lot easier to play.

## External Links

- [Discord](https://discord.gg/KjDU67x) - Community and helpdesk for D2QOL players.
- [Qolbot](https://github.com/whipowill/d2-qolbot) - Play multiplayer w/ your other singleplayer characters.
- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - Official guide to playing the game.
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - Keep track of your items as you find them.
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - See what runewords you can make.
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - Fan website w/ helpful information about the game.
- [D2 Planner](https://d2planner.github.io/skills/) - Plan your skill allocations.
- [Reddit](https://www.reddit.com/r/diablo2/) - Online forum for all the D2 fans.
- [Arq](https://www.arqbackup.com/) - App for backing up your save files.
- [ProjectDiablo2](http://projectdiablo2.com/) - These guys are taking the game to a whole new level.
- [SlashDiablo](http://slashdiablo.net/) - If you want to play the original game online, this is where you do it.
- [Loot Filter Rules](https://github.com/planqi/slashdiablo-maphack/wiki/Stats) - A list of the official loot filter coding rules.

## Credits

- D2GL by __Bayaraa__
- PlugY by __Yohann Nicolas__
- UberMod by __SnapChip__
- BaseMod, AutoPickup, QuestRewards, LinearMF, NoPenalty by __devurandom__
- FontFix, NoIntro, KeepEquip by __SnakeByteStudios__
- MapHack, LootFilter by __SlashDiablo__
- 3DSound by __IndirectSound__