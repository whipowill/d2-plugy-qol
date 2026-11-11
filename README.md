# Diablo II QOL Mod Pack

This is a mod pack for Diablo II that brings together the best quality-of-life features I have found to maximize the singleplayer experience.

![D2LOD PlugY QOL Mod Pack](https://i.imgur.com/D1CKhA2.jpg)

## Introduction

It's been 25 years and we're still playing this game.  Hats off to the [Project Diablo 2](http://projectdiablo2.com/) guys who continue to do amazing work, w/ modding capabilities second to none.  For those looking to play the vanilla experience, this modpack might be just what you're looking for.

**This repo is just for tweaks to the game engine, adding QOL features w/ no changes to the game itself.**

### Other Projects

- [Will Scarlet's Reformed](https://github.com/whipowill/d2-mod-reformed) - my soft-mod (TXT files) changes to the game
- [Will Scarlet's Qolbot](https://github.com/whipowill/d2-qolbot-go) - play multiplayer w/ your other singleplayer characters

## What's Included

- [Bayaraa's D2GL](https://github.com/bayaraa/d2gl) (v1.0.4)
	- **Widescreen** - play in widescreen 16:9 native resolutions
	- **Motion Predict** - get smoothest framerates w/ motion prediction
	- **D2FPS** - used in combo w/ D2GL and makes FPS even better, smooth as butter (v1.0.2)
- [Yohann's PlugY](http://plugy.free.fr/en/index.html) (v14.03)
	- **Infinite Stash** - store as many items as you want w/ infinite pages
	- **Ladder Runewords** - play w/ all ladder runewords available to you
	- **Infinite Respec** - reset your skill and talent points as often as you wish
- [Devurandom's Basemod](https://www.moddb.com/mods/basemod) (v1.13.9)
	- **Uber Mod** - take down Diablo Clone and the Uber bosses in singleplayer
	- **Linear Magic Find** - removes diminishing returns on magic find
	- **Quest Rewards** - pay Akara/Charsi/Larzuk to respec/imbue/socket more than once
	- **Eth Bug Fix** - fixes the famous bug on ethereal armor items (bug fix)
- [Will Scarlet's QOL](https://github.com/whipowill/d2-mod-qol)
	- **Auto Pickup** - potions, scrolls, keys, gold
	- **Keep Equip** - keep your equipment when you die
	- **No XP Penalty** - no penalty for fighting low lvl monsters or partying high level friends
	- **Merc Run** - mercenaries now run when they are following you (bug fix)
	- **Merc Equip** - mercenaries now can hold various item types consistent with their class
	- **Merc Drop** - mercenaries will now drop their gear when you hire a new one
	- **Druid Summons** - the minions you had when you logged out will auto respawn
	- **Wide Hallways** - Maggot Lair and Arcane Sanctuary now have wider hallways
	- **Auto Click** - hold down spacebar to auto-click left mouse
- [Will Scarlet's QOL UI](https://github.com/whipowill/d2-mod-qol-ui)
	- **Loot Filter** - filter out useless items w/ filter rules
	- **Buff Icons** - see what buffs and debuffs are effecting you
	- **Stat Ranges** - see the range of possible stats on items
	- **Always Show Items** - no more holding alt to show items
	- **Player Inspect** - see what another player is wearing
	- **Directions** - lines show you were to go on the map
	- **HUD Clock** - game always shows the current time
	- **Auto Party** - auto invite players to your party
- [Will Scarlet's Quartermaster](https://github.com/whipowill/d2-mod-quartermaster)
	- **Safe Storage** - a chat command system for storing common items
	- **Holy Grail** - tracks your progress on your Holy Grail quest
- [IndirectSound's 3D Sound](https://www.indirectsound.com/downloads.html)
	- **3D Sound** - enables 3D sound option in sound settings (Windows only)
- [Neuronetwork's Cinematics](https://www.moddb.com/downloads/start/222392)
	- **D2R Cinematics** - use the new cinematic cutscenes from D2R

## Install

### Windows

- Purchase keys from [Blizzard](https://us.shop.battle.net/en-us/family/diablo-ii).
- Install [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) - ``v1.12``
- Install [v1.13d patch](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) - ``v1.13d``
- Download [modpack files](https://github.com/whipowill/d2-plugy-qol/archive/master.zip) and merge the files into your D2 install directory.
- Download [cinematic files](https://www.moddb.com/downloads/start/222392) and place the contents in ``C:\Games\Diablo II\Data\local\video\eng\``.  I didn't include these files in this repo bc a) they are 500mb, and b) I don't want a copyright complaint.
- Make a ``Game.exe`` shortcut w/ target ``"C:\Games\Diablo II\Game.exe" -3dfx -direct -txt``.
- Launch the game by running the shortcut you made.

### Uninstall

Delete all the files you merged through this install process and copy the files from ``Backups`` into your ``C:\Games\Diablo II\`` folder.

## Settings

Since this mod pack includes a compilation of various mods, there are several places where you can edit things:

- ``PlugY.ini`` - stash settings
- ``BaseMod.ini`` - game settings
- ``d2gl.ini`` - video settings
- ``d2fps.ini`` - more video settings
- ``qol.ini`` - quality-of-life settings
- ``qol_ui.ini`` - maphack settings
- ``qol_ui_filter.cfg`` - loot filter settings
- ``quartermaster.ini`` - storage settings

### Loading Sequence

- ``Game.exe``
	- ``d2gfx.dll``
		- ``plugy.dll``
			- ``basemod.dll``
			- ``qol.dll``
	- ``glide3x.dll`` (this is D2GL)
		- ``d2fps.dll``
		- ``qol_ui.dll``
		- ``quartermaster.dll``

### Qolbot Compatibility

The reason I orchestrated these loading choices for the DLLs has to do with my using Qolbot.

Because Qolbot loads the game w/out ``-3dfx`` it means the bots never load D2GL, and so the bots never load the mods descended from it. This saves resources on the machine when running bots.

Also note that having World Event on in ``plugy.ini`` will cause bots to crash and disconnect.

### Loot Filter

The loot filter provided by the ``qol_ui.dll`` file uses the older Slash Diablo loot filter rules.  Edit ``qol_ui_filter.cfg`` to customize your ruleset.

See the [documentation](https://github.com/whipowill/d2-mod-qol-ui) for more on how to use this.

## Commands

- ``control-o`` - open the graphics settings

### Inventory

- ``shift + left click`` - identify an unknown item in your inventory
- ``shift + right click`` - move an item to the open stash or cube, or back
- ``ctrl + right click`` - drop an item to the ground
- ``ctrl + left click`` - sell an item if at vendor (in stock game already)

### Maphack & Loot Filter

- ``.reload`` - reload the loot filter and maphack configs
- ``+`` - increase item filter level
- ``-`` - decrease item filter level
- ``B`` - show the extensive stats screen
- ``L`` - show/hide items on the ground

### Quartermaster

Pressing the ``Insert`` key will perform the same action as the ``.deposit`` command.

- ``.deposit`` - send items from your inventory to storage
- ``.storage`` - summary of what is available from storage
- ``.storage potions|gems|runes|essences`` - display what is available in that category
- ``.take rejuv 5`` - taking rejuvination potions out of storage
- ``.take perfect skull 1`` - taking gems out of storage
- ``.take shael 1`` - taking runes out of storage
- ``.grail`` - get progress on your Holy Grail quest
- ``.grail scan`` - scan your save files for Holy Grail items

See the [documentation](https://github.com/whipowill/d2-mod-quartermaster) for more on how to use this.

## Hero Editor

One of the benefits of playing vanilla Diablo II is you can still make use of all the old tools.  When using [Hero Editor](https://www.moddb.com/games/diablo-2-lod/downloads/hero-editor-v-104), be sure to make the following changes to your ``config.ini`` file so it will still work w/ PlugY:

```
ErrorIgnore=1
LargerStashPicture=1
StashHeight=10
StashWidth=10
```

## External Links

- [The Arreat Summit](http://classic.battle.net/diablo2exp/) - official guide to playing the game
- [Holy Grail Tracker](https://d2-holy-grail.herokuapp.com/) - keep track of your items as you find them
- [Tankazon's Rune Wizard](https://fabd.github.io/diablo2/runewizard/index.html) - see what runewords you can make
- [Tomb of Knowledge](http://www.d2tomb.com/curses.shtml) - fan website w/ helpful information about the game
- [D2 Planner](https://d2planner.github.io/skills/) - plan your skill allocations
- [Reddit](https://www.reddit.com/r/diablo2/) - online forum for all the D2 fans
- [ProjectDiablo2](http://projectdiablo2.com/) - these guys are taking the game to a whole new level
- [SlashDiablo](http://slashdiablo.net/) - if you want to play the original game online
- [Hero Editor](https://www.moddb.com/games/diablo-2-lod/downloads/hero-editor-v-104) - a Windows app for editing your character files

## Credits

Special thanks to all the fans of this amazing game for keeping it alive.