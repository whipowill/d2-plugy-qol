# D2QOL | Unix

These are the instructions for using Terminal to install the Windows version of the game onto your Mac or Linux machine.  You can then easily copy the game multiple times for different mods you might want to play.

In this guide you'll end up with:

- A version of the unadulterated game
- A single-player install w/ [D2QOL](https://github.com/whipowill/d2-plugy-qol)

## Install Wine

Installing Wine is a little different on Mac and Linux.

### On Mac

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

- Install Winetricks:

```bash
$ brew install winetricks
```

### On Linux

- Install latest version of Wine (I'm using Debain-based Linux):

```bash
$ wget -nc https://dl.winehq.org/wine-builds/winehq.key
$ sudo gpg -o /etc/apt/trusted.gpg.d/winehq.key.gpg --dearmor winehq.key
$ sudo apt-add-repository "deb http://dl.winehq.org/wine-builds/ubuntu/ $(lsb_release -cs) main"
$ sudo apt update
$ sudo apt install --install-recommends winehq-stable
$ wine --version
```

- Install Winetricks:

```bash
$ sudo apt install winetricks
```

## Install Diablo II

- Create a fresh Wine directory with 32bit architecture and choose Windows 7:

```bash
$ WINEARCH=win32 WINEPREFIX=~/.wine_d2 winecfg
```

- Use Winetricks to install DXVK (this will allow you to use [D2DX](https://github.com/whipowill/d2-plugy-qol/blob/master/Guides/Video.md)):

```bash
$ WINEARCH=win32 WINEPREFIX=~/.wine_d2 winetricks dxvk
```

- Use Winetricks to nstall AutoHotKey (this will allow you to use [AutoAttack](https://github.com/whipowill/ahk-autoattack)):

```bash
$ WINEARCH=win32 WINEPREFIX=~/.wine_d2 winetricks ahk
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

- Make an alias to run the game from Terminal w/ a simple command:

```bash
$ vim .bashrc
> alias d2="cd ~/.wine_d2/drive_c/games/diablo\ ii && WINEPREFIX=~/.wine_d2 wine game.exe -3dfx -direct -txt"
```

- Reload your Terminal and play the game:

```bash
$ d2
```

## Install D2QOL

- Copy your base D2 install:

```bash
$ cp -r ~/.wine_d2 ~/.wine_d2qol
```

- Download [D2QOL](https://github.com/whipowill/d2-plugy-qol) and merge the files.
- Make an alias to run the game from Terminal w/ a simple command:

```bash
$ vim .bashrc
> alias d2plugy="cd ~/.wine_d2plugy/drive_c/games/diablo\ ii && WINEPREFIX=~/.wine_d2qol wine game.exe -3dfx -direct -txt"
```

- Reload your Terminal and play the game:

```bash
$ d2qol
```

## Extra Linux Notes

On Linux there are all kinds of tricks you have to know about to get decent game performance when using Wine.  This is the command line alias I use to optimize the game for me:

```bash
alias diablo="cd ~/Games/Windows/d2qol/drive_c/Games/Diablo\ II __NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia __VK_LAYER_NV_optimus=NVIDIA_only DXVK_HUD=fps DXVK_FRAME_RATE=100 WINEPREFIX=~/Games/Windows/d2qol gamemoderun wine Game.exe -3dfx -direct -txt"
```

- Uses PRIME Render Offload to use my dedicated NVIDIA graphics card
- Uses DXVK to set a frame rate limit of 100fps and print an FPS readout to the screen
- Uses GameMode to optimize the CPU for best gaming performance