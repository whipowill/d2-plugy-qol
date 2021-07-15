# D2QOL | Video

Special video libraries are necessary to make Diablo II run properly on modern machines.  Those video library options are:

- [Sven's Glide Library](http://www.svenswrapper.de/english/downloads.html) (older)
- [FunkyFr3sh's DDraw Library](https://github.com/CnCNet/cnc-ddraw/releases) (newer)
- [Bolrog's Glide Library](https://github.com/bolrog/d2dx/releases) (newest)

If you're on Windows then you will want to use Bolrog's Glide Library, no question about it.  If you're on Mac OSX or Linux, then you''ll want to choose between using FunkyFr3sh's DDraw Library or Sven's Glide Library.

D2QOL comes will all three of these options pre-installed.  See the instructions below on how to activate the proper library for you.

## Bolrog's Glide Library

- The necessary files are already included in the D2QOL files you merged into your game directory.
- Just make sure your game shortcut target includes ``-3dfx -direct -txt``.

## FunkyFr3sh's DDraw Library

- The necessary files are already included in the D2QOL files you merged into your game directory.
- Edit the ``Plugy.ini`` file to include ``|D2HD.dll`` in the loaded DLLs list (line 25).
- Open ``regedit`` on your Windows machine:
	- Navigate to ``HKEY_CURRENT_USER\Software\Blizzard Entertainment\Diablo II\VideoConfig``.
	- Change the ``Render`` value to zero.
- Modify your game shortcut target to include ``-direct -txt`` (do not use ``-w -3dfx -nofixaspect``).

The shaders that upscale the graphics will work on Windows, Linux, and now even Mac.  For Mac, you may have to manually edit the ``GLSL`` file to have ``#version 150`` at the top of the file.

### Wine

If you're using Wine you'll have to use the command line.

- Edit the registry:
```bash
$ WINEPREFIX=~/.wine_d2plugy regedit
> Navigate to HKEY_CURRENT_USER\Software\Blizzard Entertainment\Diablo II\VideoConfig.
> Change the Render value to zero.
```
- Edit the Wine config:
```bash
$ WINEPREFIX=~/.wine_d2plugy winecfg
> On the Applications tab, run as Windows XP.
> On the Libraries tab, add override for "ddraw".
```
- Modify your Terminal alias:
```bash
$ vim .bashrc
> alias d2plugy="cd ~/.wine_d2plugy/drive_c/games/diablo\ ii && WINEPREFIX=~/.wine_d2plugy wine game.exe -direct -txt"
```
- Reload your Terminal and play the game:
```bash
$ d2plugy
```

## Sven's Glide Library

- The necessary files are already included in the D2QOL files you merged into your game directory, but they're in the wrong location.
- Copy the files in the ``Glide`` folder and paste them into the game directory, overwriting the ``glide3x.dll`` that's already there (Bolrog's).
- Edit the ``Plugy.ini`` file to include ``|D2HD.dll`` in the loaded DLLs list (line 25).
- Run the ``glide-init.exe`` file and modify the settings:
	- Switch to ``English``.
	- On the ``Settings`` tab:
		- Turn on ``window-mode``.
		- Turn on ``keep aspect ratio``.
		- Turn on ``centerered``.
	- On the ``Renderer`` tab:
		- Turn on ``32 bit rendering``.
		- Turn on ``texture for videos``.
		- Turn on ``bilinear filtering``.
		- Turn on ``no gamma``.
	- On the ``Extensions`` tab:
		- Turn on ``MGL_EXT_swap_control``.
- Modify your game shortcut target to include ``-w -3dfx -nofixaspect -direct -txt``.

### Wine

If you're using Wine you'll have to use the command line.

- Run the ``glide-init.exe`` executable:
```bash
$ cd ~/.wine_d2plugy/drive_c/games/diablo\ ii
$ WINEPREFIX=~/.wine_d2plugy wine glide-init.exe
```
- Modify your Terminal alias:
```bash
$ vim .bashrc
> alias d2plugy="cd ~/.wine_d2plugy/drive_c/games/diablo\ ii && WINEPREFIX=~/.wine_d2plugy wine game.exe -w -3dfx -nofixaspect -direct -txt"
```
- Reload your Terminal and play the game:
```bash
$ d2plugy
```