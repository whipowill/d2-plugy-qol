Readme for the GLIDE3-to-OpenGL-Wrapper Version 1.4e (c) 2010 by Sven Labusch

content:
1. Preface
2. Files included
3. Requirements
4. Installation/Deinstallation
5. File-descriptions
6. References/technical aspects
7. Version history
8. frequently asked questions
9. other


				1. Preface


First of all: Hello everybody!
To make it short: i was disappointed about the performance Diablo2 shows in the Direct3D-mode.
Because of the fact that the game runs far better in GLIDE-mode, I tried to find a way, to make the game run in GLide-mode even on my computers at home. There were two problems:
1. Glide-Device-Driver exist only for Voodoo-graphiccards. Diablo2 needs at least a Voodoo-Card of the Voodoo-Rush-type, but my computers had "only" Geforce2MX-cards.
2. there are many GLIDE-wrappers, but I haven't found any that runs fine on my computers.
The patch 1.10 for the game didn't bring any improvements, so I decided to write my own wrapper, where I again want to point out:
This GLIDE-wrapper is explicitly written for the game Diablo2 (and its expansion "Lord of Destrucion", of course;)). You have to assume that it won't work together with other programs or at least that it will produce incorrect output.

Supplement:
This is the version 1.4e of the wrapper.
Big thanks go to "Seltsamuel", "Shabazza", "Luzi", "mindphlux", "UnserenToten", "ChaosEnergy", "acesulfam", "Seltsamuel"  and the staff from the indiablo.de-forum.


				2. Files included


4 files:

glide-liesmich.txt  34366 bytes
glide-readme.txt    29538 bytes
glide-init.exe      134144 bytes
glide3x.dll         138752 bytes



				3. Requirements


needed (so it may run):
- OpenGL supporting Graphiccard
- same requirements as the game
recommended (so it runs well):
- Graphiccard that supports OpenGL1.3-Extensions
- Graphiccard equal to Geforce256 or better with at least 32MB video-memory
- at least 256MB main-memory
NOT recommended ('cause it might run worse than before):
- any type of graphiccard that uses a shared memory architecture
You can try it nevertheless, but I think it's quite improbable.


				4. Installation/Deinstallation


There are two possibilities for installation:
1. Copy the file "glide3x.dll" into the windows-system-directory (i.e. "c:\windows\system").
2. Copy the file "glide3x.dll" into the game-directory (i.e. "c:\games\diablo2").

'cause of the fact that this wrapper ist explicitly written for this one game, I would prefer the 2nd way.
Once the files are copied, you have to run the Vid-Test of the game and to choose Glide.

For deinstallation I prefer the following:
1. start the glide-init.exe, there choose "std/export" and click on "+remove registry-entries".
2. delete the wrapper-files.
3. run the Vid-Test of the game and choose a different graphic-mode.


				5. File-descriptions


  glide-readme.txt
That's the file you are reading now.

  glide-liesmich.txt
Like the glide-readme.txt, but in german.

  glide3x.dll
Thats the base-file of the wrapper.
If the wrapper recognizes an error, a file named "gl32ogl.err" will be created, in that the problem will be described.

  glide-init.exe
Here you can change some settings of the wrapper, the program is splittet into several areas:
on the left, there is the main-menu,
in the middle, you are able to change the values themselves,
on the right is an info-screen, where some small informations can be displayed,
and at the bottom is a file reader, where you can read the glide-readme.txt (or glide-liesmich.txt).
The settings are stored into the registry.

In the main-menu, you can choose out of the following menus:

OpenGL-infos
settings
renderer
Wrapper-statistics
Extensions
std/export
Test
English/Deutsch
Quit

Depending on the menu you chose, the following values can be changed:

    OpenGL-infos:

Here, you can't change anything directly. This menu exists for getting some Informations from the installed OpenGL-Driver, like how much texture-memory is available, how large the textures can be, what extensions are supported, ...
These Informations have to be queried manually by klicking on "Query OpenGL-infos".
It is possible, that the OpenGL-driver on the computer misbehaves in the test-run, after OpenGL-infos were queried. In this case, please first finish and restart the program before restarting a test.

    settings:

Here you can change some more general settings of the wrapper.

window-mode:
 If activated, the wrapper renders the game-graphics into a window, if deactivated, the graphics are displayed in fullscreen. This setting overrides the "-w"-command-line-parameter, but anyhow, I recommend to use the "-w" Parameter if you want to play in window-mode: the mouse then doesn't jump around if you open the inventory via keyboard.

captured mouse:
 If activated, the mouse cannot leave the game-window.

keep aspect ratio:
 if activated and running in window-mode or at desktopresolution, the game-scene will be rendered in a fixed 4/3-aspect-ratio. Additional space in the window/at the desktop will be filled in black color.

vertical synchronization(VSYNC):
 if activated, the framerate of the game will be capped at the refreshrate of the monitor. Thats quite useful: If the monitor can only display 100 frames per second, why should the game render 150 ones? 50 of them would be wasted?
Ok, you could see, how much additional load could be handled by the hardware,
but I think that's all .....

fps-limit:
 here you can define the maximum framerate that may be achieved by the wrappe. Is only neccessary if VSYNC does not work and if you want to preserve the processor and graphiccard.

static size:
 here you can define, if the game-window has to be stretched to a certain size. If a certain size is chosen and the wrapper runs in fullscreen-mode, the surrounding area is filled black.

window extras:
 If activated and running in window-mode, you have the possibility to scale the window in size. The window content will be scaled up/down to fit into the new size: so the graphic doesn't get better.

centered: (only in window-mode)
 If activated and running in window-mode, the window is centered onto the desktop automatically.

remember position: (only in window-mode)
 if activated, the wrapper saves the window-position, so that at game-start the window appears at the old position again.

refreshrate: (only in fullscreen)
 If running in fullscreen-mode, you can choose here, what display-refreshrate should be set up for the monitor. The possibilities depend on the hardware, operating system, drivers etc.

desktopresolution: (only in fullscreen)
 If activated and running in fullscreen-mode, the monitor-resolution will not be changed by the wrapper anymore, so the game is running in the desktopresolution. I added this option, 'cause I have seen some TFT-displays which aren't able to display the resolution 800x600 (or 640x480) in a acceptable quality (or at all).
But like for "window extras": this doesn't increase the game graphics quality (normally).

    renderer:

Here you can make some settings concerning the wrapper-render-engine itself:

texture-memory:
 here you can choose, how much available texture-memory has to be told to the game.
You have to be aware, not to choos a too big value: the graphiccard-driver could be forced to out-source textures. There are also some drivers, which can't handle the textures, if you chosse a too high value: texture-glitches appear.
The optimal value depends on the hardware, the settings and the driver. If you queried the OpenGL-infos, there will be made a suggestion on the right hand side. But that value is rounded to floor, so a higher performance might be achieved, if you set the texture-memory a little bit higher.

buffer-texture-size:
 Here you can change the size of the textures, the wrapper uses to buffer the textures of the game. The smaller the buffer-textures, the more game-textures fit onto the graphiccard,
but the larger the buffer textures, the more game-textures fit inito one single buffer-texture.....
The best value depends on the graphiccard and the texture-memory, but I think 1024x1024 is a quite good value.

32 bit rendering:
 If activated and rendering in fullscreen-mode, the display will be set up with 32bit color-depth and the wrapper renders in 32bit, too.
 I added this option, 'cause there might be some drivers, which can't handle the 16bit-mode that is normally used.

texture for videos:
 if activated, videos won't be shown on the display directly, but via a texture. There are enough drivers where this works far better, so its activated in general.

bilinear filtering:
 if activated , the wrapper renders the scene to a texture first, and from there on the screen. This extra-step reduces the framerate but increases the image-quality if desktopresolution is activated.

supersampling:
 if activated and "WGL_ARB_render_texture" is activated,too, the rendering will be done in a 4times higher resolution, this costs additional performance but benefits in a sharper image-quality.

shader-gamma:
 if activated and supported by the driver, the gamma-/contrast-settings will be realized by shaders instead of the monitor-settings. This reduces the performance again, but has some benefits: screenshots are automatically gamma-correct, in window-mode the gamma-setting only affects the window.

no gamma:
 if activated, the wrapper won't touch the gamma-settings.

keep desktop composition:
 if activated, the wrapper leaves the setting for desktop composition untouched. If deactivated, the wrapper deactivates desktop composition as long as the game is running.

    Wrapper-statistics:

Here you can change the settings, about what statistical informations have to be shown by the wrapper.

corner for infos:
 This parameter defines in what corner of the screen these informations have to be displayed.

framerate:
 If activated, the wrapper displays the framerate of the game. This value is computed once per second and independent of the framerate-info of the game itself. So these values might differ from each other a little bit.

clock:
 If chosen, the wrapper displays the system-time of the computer (in the chosen appearence). The clock-value is the same as the one in the task-bar.

texturemass:
 If activated, the wrapper displays the amount of texture-memory, that is needed for storing the game-textures. This value should stay below of the real amount of texture-memory the graphic-card has. If it raises too high, I recommend to set the texture-memory of the wrapper to a lower value.

sequence:
By clicking on this button, you can chose, in what sequence the chosen values have to be displayed (what's at the top, what at the bottom,...). On the right hand side in the Parameter-infos-area, you can see, in what order these infos will be currently shown. If you have chosen, to see only 2 values, you might have to click twice for swapping the order.

    Extensions:

Here you can chose, which extensions have to be used by the wrapper. In general, you don't need to deactivate one of them, except the OpenGL-driver has some problems or you want to test something....

GL_EXT_vertex_array:
 If activated and supported, the vertex-data won't be sent to the driver step by step: it will be collected into one single array and then the array will be sent in one step to the driver.

GL_ATI_fragment_shader:
GL_ARB_fragment_program:
GL_EXT_paletted_texture:
 If at least one of these extensions is activated and supported by the driver, the wrapper can use the 8-bit-game-textures directly. I all three are deactivated or not supported, the wrapper has to emulate these textures via 16-bit-textures what needs additional texture-memory and some time for converting.
If more than one of these extensions is activated and supported, the EXT-one stands above the ARB-one. The ATI-one has the lowest importance of these three.

GL_EXT_shared_texture_palette:
 If the wrapper uses GL_EXT_paletted_texture, you can define with this extension, if the buffer-textures have to use all the same color-palette, or if they all have to use their own one (which have then to be filled with the same values...).

GL_EXT_packed_pixels:
 If the wrapper has to emulate the 8-bit-textures of the game, this extension increases the speed of texture-realoding.

GL_EXT_texture_env_combine:
 If the wrapper doesn't use GL_ATI_fragment_shader or GL_ARB_fragment_program, this extension has to be used to draw some transparency-effects. But that shouldn't be such important.

WGL_EXT_swap_control:
 If activated and supported, this extension makes the manual control over the vertical synchronization available.

WGL_ARB_render_texture:
 if activated and supported, the wrapper renders the scene to a texture first, and from there on the screen. This extra-step reduces the framerate but increases the image-quality if desktopresolution is activated or the window-size has been changed.

    std/export:

In this menu, you can restore the default settings of the wrapper. You can also export the wrapper-settings into a txt-file.

restore default values:
 Simply restores the default values.

+remove registry-entries:
 The keys, generated to store the settings in the registry will be deleted, too.

export settings:
 opens a dialogue-window for choosing/creating a save-file. The wrapper-settings will then be exportet into this file.

    Test:

With this button, you can do a small test-run, to see if the wrapper works at all, without needing to start the game itself. In my opinion this test should gain at least 50FPS, but I think that shouldn't be normally the problem...

    English/Deutsch:

Here you can choose, in what language the wrapper and  the frontend have to appear.

    Quit:

Leaves the frontend.


				6. References/technical aspects


hmm, ok, where shall i begin? Ah yeah, let's start, what this wrapper makes such different to the Direct3d-mode:
1. the Direct3d-mode of Diablo2 creates far less textures than the Glide-mode, so the Direct3d-engine has to reload the textures more often.
2. the wrapper uses OpenGL, the Direct3d-mode DirectX6. DirectX6 does not support 8-bit-textures.
3. the texture-administration differs between DirectX,OpenGL and Glide:
The overhead for administration in DirectX is enormous, compared to OpenGL or Glide. So OpenGL and Glide have their advantages when using dynamic textures. And here's the key: Diablo2 has so much textures, that they won't fit on any graphiccard, so nearly all of the textures have to be loaded dynamically. And in this point Direct3D fails totally: the dynamic loading of textures is damn slow (in OpenGL its average).
As a work-around of this issue, the wrapper has to create some more physical textures , than are used in Glide. It is posssible, that the wrapper creates 24MB physical textures, when it it set to emulate only 16MB voodoo-texture-memory, but this depends also on the settings.

I want to mention, that you don't have to make hasty reproaches at Blizzard's programmers:
if you turn back time and look at the technical state of the art, as it was, when the game had been programmed, you had the problem, that you had to economize the few resources which were available. With this in mind, the Direct3d-engine of Diablo2 uses as much performance as is reachable with DirectX6. But that's not much, or "state of the art" has changed, so that it could be more if you write a whole new engine..... and switch to OpenGL .... or the graphiccard-manufacturer release REAL Glide-device-driver.

But back to the wrapper itself.
it uses (as already mentioned) OpenGL and has some requirements.
following OpenGL-extensions are needed for totally correct rendering:
GL_EXT_texture_env_combine
GL_EXT_bgra
the following OpenGL-extensions are favourable:
GL_EXT_vertex_array
GL_ATI_fragment_shader
GL_ARB_fragment_program
GL_EXT_paletted_texture
GL_EXT_shared_texture_palette
GL_EXT_packed_pixels
WGL_ARB_render_texture

so a graphiccard providing OpenGL1.3 is needed for correct rendering.
if one of the extensions GL_EXT_paletted_texture,GL_ATI_fragment_shader and/or GL_ARB_fragment_program is provided, the wrapper can use 8bit-textures instead of 16bit-textures, what speeds up the texture-reloading significantly.

The wrapper uses OpenGL, that's why there is the 60Hz-bug, too, if you have Windows2000 or WindowsXP installed as the operating system and if the wrapper is not told to set the monitor-refresh-rate manually.
There are many solutions for solving this problem: just search the web or take a look into the internet-presentations of some game-magazines.


				7. Version history


Version 1.4e:
in the glide3x.dll
small bugs concerning captured mouse and taskswitching patched
the wrapper now realizes, that D2 doesn't minimize the window anymore, if the game-windows looses the focus.
static size of 1280x1024 fixed to 1280x960
in the glide-init.exe
the wrapper-settings can now be exportet into a txt-file

Version 1.4d:
in the glide3x.dll:
framerate-limit included.
static window-size included.
the wrapper can save the window-position now.
32bit is now standard
GL_EXT_vertex_array is now deactivated as standard
32MB  simulated texture-memory is now standard
in the glide-init.exe:
the graphiccard-texturememory-throughput is now shown in a diagram. By this diagram you can tell the wrapper of how many texture-memory it should estimate.

Version 1.4c:
in the glide3x.dll:
fixed a bug concerning GL_EXT_vertex_array. This extension should work now even with newer graphic-card-drivers.
wide-screen-correction can now manually de-/activated
fixed several bugs concerning wrapper-statistics
added a workaround concerning the "gidbinn-bug"
in the glide-init.exe:
the available texture-memory is now detectet via OpenGL
the available texture-memory is capped at 256MB
the testrun has been fixed so that it works even with real 3dfx-cards

Version 1.4b
in the glide3x.dll:
fix a bug, that occured if captured mouse was activated and the game were switched from window-mode to dektop-resolution via ALT-ENTER
render to texture splittet into WGL_ARB_render_texture and bilinear filtering
in the glide-init.exe:
fixed some minor bugs

Version 1.4a
in the glide3x.dll:
at desktop-resolution, widescreen-resolutions will be recognized
modified the texture-palette for shader use
fixed some minor bugs
in the glide-init.exe:
fixed some minor bugs

version 1.4
in the glide3x.dll:
reprogrammed the internal texture-managing: the textures are handled more efficiently now.
8-bit-textures can be simulated by shaders now. The texture-reloading is faster this way instead of using 16-bit textures.
VSYNC can be set on/off by the wrapper itself now.
"DirectX for videos" removed
in the glide-init.exe:
fsaa/multisampling removed : it's useless here
fixed gammaramp removed
render to texture added
supersampling added
shader-gamma added
no gamma added
reprogrammed the frontend totally.
Settings are stored in the registry now.
OpenGL-infos can be queried now, so that some small hints can be given to the wrapper-settings.
The frontend contains a file-reader now, that displays the reademe-files of the wrapper.
Added a test-routine, so that the wrapper can be tested without using the game itself.
btw: filenames slightly changed again

version 1.3c
in the glide3x.dll:
the wrapper renders now into its own window, presented inside the D2-window.
Only that's why its possible to set multisampling, or to make the d2-window sizable.
"smooth resolutionchange" is not necessary anymore.
DirectX is only used for videos now, if at all.
But no changes made to the render-engine.
in the gl32ogl-init.exe:
"smooth resolutionchange" removed
"DirectX for initialization" changed to "DirectX for videos"
"texture for videos" added
possibility to set the monitor-refresh-rate added
"window extras" added
"desktopresolution" added
possibility to set Multisampling/FSAA added
"sort order" renamed to "sequence"
in the "readme"s:
faq added
btw: filenames slightly changed


version 1.3b
in the glide3x.dll:
combiner-modes changed, the problem with the texture-outlines ist solved, switching between combiner-modes ist faster now.
If GL_EXT_vertex_array is not provided by the Graphiccard, the wrapper uses its own routines, so the wrapper works on those machines, too. GL_EXT_texture_env_combine and GL_EXT_bgra are not totally necessary anymore. But there will be glitches, if they are not provided by the driver. Changes made to the settings of the wrapper are taken on the fly: switch back to desktop, change settings, turn back to game, ready.
in the gl32oglinit.exe:
Frontend changed
switch for info sort order added
switch for language-change added
renamed the "readme.txt" to "liesmich.txt" and translated it to the now english version "readme.txt"

version 1.3a
in the glide3x.dll:
few changes at the combiner-modes. Compatibility-issues should be appear less often.
in the gl32oglinit.exe:
switches added:
"Uhr"
"zentriert"
"DirectX zum Einrichten"
"feste Gamma-Tabelle"
"Maus begrenzen"

version 1.3
in the glide3x.dll:
GL_EXT_vertex_arrays are used and required. The wrapper can be advised to not switch back to desktop-resolution first when changing resolution. Joining/leaving a game is far faster this way, but when switching manually to the desktop, the resolution stays at the game-resolution.
in the gl32oglinit.exe:
switch added: "weicher Auflösungswechsel"

version 1.2
in the glide3x.dll:
texture-management of the wrapper modified, so that less processor-power is needed, but therefor more physical texture-memory is needed. Beside of the framerate it is possible to let the wrapper show, how much physical textures are created.
in the gl32oglinit.exe:
switch added: "stats"
range for the texture-memory reset to 8MB-108MB

version 1.1
in the glide3x.dll:
changed the texture-memory-configuration told to the game, the game manages the textures more efficiently. Upload of 16Bit-textures changed.
in the gl32ogl.exe:
splitted the switch "8-Bit-Texturen" into three switches:
"GL_EXT_palettized_textures"
"GL_EXT_shared_texture_palette"
"GL_EXT_packed_pixels"
default setting for texture-memory reset to 16MB
range for the texture-memory reset to 8MB-64MB


				8. frequently asked questions


Since I released the wrapper, i have been asked several questions because of problems that might occur with the wrapper. Here I want to handle the most frequent ones.

1. If I use the wrapper with Diablo2, the framerate drops down significantly (to somewhere around 1 fps), and possibly in wrong colors, too.

The wrapper uses OpenGL and that's why it is necassary, that the computer has correctly working OpenGL-drivers. There are multiple possibilities why the wrapper isn't able to work correct together with the driver.
Solutions I have found so far:
- reinstall the gaphics-drivers
- if you have more than one monitor attached: deactivate the secondary ones in the display-properties.

For older graphic-cards it's possible that there are no OpenGL-drivers at all. In this case, there helps only a complete change of the card.

2. the wrapper runs, D2 has a correct image, but the framerate is exact the same as before.

in general the wrapper has a problem: from the point of view of the whole system (the complete computer), the wrapper is only additional load. To increase the framerate instead of decrease it, the wrapper tries to distribute the load more to the graphic-card. But if the graphic-card is the reason, why the framerate is low (a 3GHz-system with a Riva128 for example), then it's not surprising, if the framerate with the wrapper is lower than without it.
possible solutions:
hardware-side:
- find out, what is the slowest part of the computer, and change it with a better one: an 3GHz processor and a GF5900 are useless if there are only 64MB main-memory, for example.
software-side:
- install newer/other drive. There are several components (like the graphiccard) for which there are more than one driver, and the newest isn't ever the best...
- background-applications can reduce the performance,too. Viruses, worms and trojans, too, of course.
- if the game runs in window-mode via "-w"-parameter, make sure that the "-3dfx" parameter is included in the shortcut: otherwise D2 uses neither Glide nor Direct3D.

3. I am playing in single-player and the framerate won't go over 25fps.

That's normal in single-player: the framerate is capped at 25fps.
If you want to play your local heros at higher framerates, you have to host a multiplayer-game (it's equal if open bnet or tcp/ip).

4. I'm playing in multi-player-mode, but with the wrapper the framerate won't go over 60fps.

It seems that the monitor is set to a refreshrate of 60Hz. It might be, that the monitor is not able to work with higher refresh-rates (like TFT-displays), or it is the "60Hz-bug" of Win2K/XP.
Some display-drivers have tools to avoid this problem, or you might choose in the wrapper-frontend, what refresh-rate to use. But this depends on the hardware and drivers.

5. The framerate is higher than 60fps, but it stays at (f.e.) 90fps. But other people have a even higher framerate with worse hardware (f.e. 200fps)

In general, the display driver caps the framerate at the monitor-refresh-rate. That's quite normal: why to render 200 frames per second, when only 90 of them can be displayed? (110 of them are totally wasted)
Beside of posing, this provides the possibility to see, how much additional load the computer can handle, before it becomes choppy.
This framerate cap is called "vertical synchronization" and can be de-/activated via the display-propertiesor or in the wrapper-frontend.

6. sometimes the display is dimmed.

The wrapper had no chance to set the gamma-ramp.
solutions I have found so far:
- reset gamma or contrast in the game
- try to find out, if a background-application sometimes tries to access the display and disable it.
- reinstall the display drivers
- take a look, if the display drivers support some kind of brightness-control
- if supportet by the opengl-driver: activate shader-gamma in the front-end

7. I have installed some mods for the game, does the wrapper work with them, too?

I have programmed the wrapper for the original version of the game, 'cause I don't have the time to test it with every single mod. That's one thing you have to do by yourself.
But as far as I can see, I can say:
the wrapper should work with EVERY mod, or with other words:
the mods should work with the wrapper as good as without it.

I have only tested the wrapper in combination with the chaos-empire-mod (because I'm playing this mod), and there I haven't seen any incompabilities. There were no complains from "official" side,too.
I have tested the "d2-accelerator", too (and I haven't seen any faults,too). But I have heard of problems with the mod itself.

8. I have installed the wrapper, runs well, but can I boost it even more?

In general,if the wrapper is running with the standard-settings, you can improve the performance with the "texture memory" parameter.
What setting is best depends on the hardware. I think the following guidelines seem to be quite well:
on graphic-cards that support the 8-bit-textures (f.e. all Geforces an Radeons since 8500):
texture memory= real video-memory / 4 *3
on any other graphic card:
texture memory= real video-memory / 8 *3

9. I'm playing with the wrapper in windowed mode, but everytime I open the inventory, the mouse jumps to the wrong place.

The problem is based on the fact, that the game itself wasn't started with Window-capability. Make sure that in the link you used to start the game, the parameters "-w" AND "-3dfx" are included.
f.e.:
"c:\games\Diablo II\Diablo II.exe" -w -3dfx

10. Vista, if I start the wrapper, only a black screen/window appears and in the upper left corner of the screen some characters are shown slowly one by another.

Please make first sure, if the Aero-Glass theme is activated. If it is so, please first try to deactivate it.
The wrapper uses the OpenGL-interface. In Vista, the real OpenGL-interface is not supportet, if Aero-Glass is activated.
In the start-link of Diablo2 you can set, that at game-start the Aero-Glass theme will be deactivated automatically. And at ending the program automatically activated again:
in the properties of the D2-start-link go to compatibility, set there the mark at 'Disable desktop compositing'.
The wrapper can disable Aero-Glass temporarily, too. Just unmark at "renderer" the button "keep desktop composition".


				9. other


This wrapper is freeware, it may be copied as long as the files stay unchanged and altogether.
At the programming, my highest priority was to make a stable running program, but unfortunately I can't give any warranty that the wrapper runs perfectly on every system. There are too much possibilities which could cause the wrapper to malfunction. So you have to use this program at your own risk.

But anyway: on the computers where I use this wrapper now, I have a significantly performance-increase.
bye
 Sven Labusch