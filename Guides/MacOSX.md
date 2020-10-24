# D2QOL | Mac OSX

These are the instructions for using Terminal to install the Windows version of the game onto your machine.  You can then easily copy the game multiple times for different mods you might want to play.

In this guide you'll end up with:

- A version of the unadulterated game
- A single-player install w/ [PlugY](http://plugy.free.fr/en/index.html)

## Install Wine

- Use [Homebrew](https://brew.sh/) to install Wine:

```bash
$ brew install wine
```

- If using Mac OSX Catalina or later then use this brew tap instead:

```bash
$ sudo spctl --master-disable // to disable gatekeeper and prevent annoying security popups
$ brew tap gcenx/wine
$ brew cask install --no-quarantine wine-crossover
```

## Install Diablo II

- Create a fresh Wine directory and choose WinXP:

```bash
$ WINEARCH=win32 WINEPREFIX=~/.wine_d2 winecfg
```

- Download [Diablo II](https://mega.nz/#!e9thyD6A!ExGJuZUtvRJ2c8DrxSL0ihCouh-ARbdVxODXIqVt3dc) and the [v1.13c](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113c.exe) or [v1.13d](http://ftp.blizzard.com/pub/diablo2exp/patches/PC/LODPatch_113d.exe) patch, and move them into the Wine directory:

```bash
$ cd ~/.wine_d2/drive_c
$ mkdir games
$ cd games
$ open .
```

- Run the EXE files to install the game:

```bash
$ WINEPREFIX=~/.wine_d2 wine /your/path/to/d2/installer.exe
$ WINEPREFIX=~/.wine_d2 wine /your/path/to/d2lod/installer.exe
$ WINEPREFIX=~/.wine_d2 wine /your/path/to/patch.exe
```

- Install a graphics library (``Glide`` or ``DDraw``) by following this [guide](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Video.md).
- Make an alias to run the game from Terminal w/ a simple command:

```bash
$ vim .bashrc

// if using glide
> alias d2="cd ~/.wine_d2/drive_c/games/diablo\ ii && WINEPREFIX=~/.wine_d2 wine game.exe -w -3dfx -nofixaspect"

// if using ddraw
> alias d2="cd ~/.wine_d2/drive_c/games/diablo\ ii && WINEPREFIX=~/.wine_d2 wine game.exe -nofixaspect"
```

- Reload your Terminal and play the game:

```bash
$ d2
```

## Install PlugY

- Copy your base D2 install:

```bash
$ ditto ~/.wine_d2 ~/.wine_d2plugy
```

- Download [PlugY](http://plugy.free.fr/en/index.html) and run the install:

```bash
$ cd ~/.wine_d2plugy/drive_c/games
$ open .
$ WINEPREFIX=~/.wine_d2plugy wine /your/path/to/plugy.exe
```

- Make an alias to run the game from Terminal w/ a simple command:

```bash
$ vim .bashrc

// if using glide
> alias d2plugy="cd ~/.wine_d2plugy/drive_c/games/diablo\ ii/mod\ plugy && WINEPREFIX=~/.wine_d2plugy wine plugy.exe -w -3dfx -nofixaspect -direct -txt"

// if using ddraw
> alias d2plugy="cd ~/.wine_d2plugy/drive_c/games/diablo\ ii/mod\ plugy && WINEPREFIX=~/.wine_d2plugy wine plugy.exe -direct -txt"
```

- Reload your Terminal and play the game:

```bash
$ d2plugy
```
