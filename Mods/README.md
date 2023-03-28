# D2QOL | Soft Mods

Included in this folder are several "soft mods" that are popular in the D2 community which include changes to inventory, drops, mercenaries, skills, and more.

These mods are separated into individual folders so you can pick and choose what you want.  None of these mods are turned on by default in this modpack, you have to turn them on yourself.

To install any of these, just copy and paste the individual folder contents into ``C:\your\path\to\Diablo II\Data\Global\Excel\``.

### CUBEMOD

Code by [whipowill](https://github.com/whipowill).

- Upgrade 2 runes -> 1 higher rank rune
- Downgrade rune -> 2 lower rank runes
- Upgrade 3 gems -> 1 higher rank gem
- Downgrade gem -> 3 lower rank gems
- Use a key w/ a socketed item and get the runes back
- Socket any item (including unique or set items) w/ a Hel Rune

### DROPMOD

Code by [whipowill](https://github.com/whipowill).

- Countess always drops 3 runes
	- Normal up to Lem
	- Nightmare up to Vex
	- Hell up to Cham
- Mobs always drop maximum amount of loot
- Bosses always drop quest loot

### INVENTORYMOD

Code by [devurandom](https://www.moddb.com/mods/basemod), modified by [whipowill](https://github.com/whipowill).

- Mercenary can equip all item slots
- Stash becomes 10x10 (from 6x8)
- Inventory becomes 10x6 (from 10x4)
- Cube is unchanged

### LEVELMOD

Code by [whipowill](https://github.com/whipowill).

- All maze levels are same size, regardless of difficulty
- New level 85 areas in Hell:
	- Act 1
		- Tristram
		- Crypt
		- Mausoleum *
		- Pit *
		- Cathedral
		- Catacombs
	- Act 2
		- Stony Tomb
		- Maggot Lair
		- Ancient Tunnels *
		- Tal Rasha's Tomb
	- Act 3
		- Swampy Pit
		- Flayer Dungeon
		- Ruined Temple
		- Disused Fane
		- Forgotten Reliquary
		- Forgotten Temple *
		- Ruined Fane *
		- Disused Reliquary *
		- Durance of Hate
	- Act 4
		- City of the Damned
		- River of Flame *
		- Chaos Sanctuary *
	- Act 5
		- Infernal Pit
		- Pit of Acheron
		- Abaddon
		- Worldstone Keep *
	- Pandemonium
		- Sinking Sands
		- Matron's Den
		- Furnace of Pain
		- Uber Tristram

### MERCMOD

Code by [whipowill](https://github.com/whipowill).

- Act 1
	- Blessed Aim
	- Fire - Fire Arrow / Exploding Arrow
	- Ice - Cold Arrow / Ice Arrow
- Act 3
	- Meditation
	- Fire - Inferno / Fireball
	- Lightning - Charged Bolt / Chain Lightning
	- Cold - Ice Blast / Glacial Spike
- Act 5
	- Might
	- All - Bash / Stun

### MONSTERMOD

Code by [whipowill](https://github.com/whipowill).

- [Bone Fetish](http://classic.battle.net/diablo2exp/monsters/act3-bonefetish.shtml) death explosion disabled
- [Tomb Viper](https://www.reddit.com/r/diablo2/comments/r7m6qm/tomb_vipers_a_history/) removed from the game

### SKILLMOD

Code by [whipowill](https://github.com/whipowill).

- Barbarian
	- Melee weapons spawn w/ splash damage
	- Thrown weapons spawn w/ replenishing quantity
	- Leap, Shout, Battle Orders, Battle Command allowed in town
- Amazon
	- Magic and rare quivers are possible and are replenishing
	- Dodge, Avoid, Evade bug fixed (per technique by [Nagahaku](https://d2mods.info/forum/viewtopic.php?p=500423&sid=923afb1f8828e76713d3c8a1f9f78ff1#p500423))
- Sorceress
	- Teleport allowed in town and makes less irritating sound
	- Meteor lands 2/3 faster and makes less irritating sound
- Druid
	- Shapeshift lasts longer
	- All beasts can be summoned at same time
	- Spirits & vines cannot die
	- Teleport allowed in shapeshift form

#### Discussion

Adding automagic affixes to weapons is a pretty invasive change and there is no going back.  If you wanted to install w/out making such a big change, you would delete ``Weapons.txt``, ``UniqueItems.txt``, and ``SetItems.txt`` to disable that effect.

Alternatively, there are some jewels in these files that will also grant ``splash`` and ``rep-quant``, but I have them disabled.  You would edit the ``MagicPrefix.txt`` and ``MagicSuffix.txt`` files to make those new jewels spawnable if you wanted them.

- Jewels
	- "Brute's" and "of the Brawler" grant splash damage
	- "Quartermaster's" and "of Renewal" grant replenishing quantity

## External Links

- [TXT Files](https://github.com/whipowill/d2-113c-txt) - A repository of the original game files.
- [TXT Changelog](https://github.com/whipowill/d2-113c-txt-changes) - A repository cataloguing every change to the game files I've made.
- [Phrozen Keep](https://d2mods.info/forum) - The forum of master D2 modders and their ancient discussions.
- [MPQ Editor](http://zezula.net/en/mpq/download.html) - App for unpacking MPQ files (handy for reverse engineering what others have done).
- [Unix2Dos](https://phoenixnap.com/kb/convert-dos-to-unix) - Command line tool for converting file endings (handy for modding TXT files)
- [XVI32](http://www.chmaas.handshake.de/delphi/freeware/xvi32/xvi32.htm#download) - Freeware hex editor XVI32.
- [AFJ](https://d2mods.info/forum/viewtopic.php?t=15454) - Table editor for game strings.