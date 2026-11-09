BACKUPS
=======

Original, unmodified copies of the game files that were changed in ../ (the src folder).
Put one back to undo the change described next to it.

D2gfx.dll
  Original 1.13c file.
  In src it has the PlugY loader patched in: after the renderer DLL loads, it calls LoadLibrary("PlugY.dll") and
  PlugY's _Init@4(0), and _Release@4 on unload. PlugY in turn loads the other DLLs listed in PlugY.ini
  (DllToLoad=Basemod.dll|BH.dll|autopilot.dll), so the autopilot mod is started through this hook.

Patch_D2.mpq
  Original Blizzard 1.13c patch archive (3,915,305 bytes).
  In src it is a rebuilt data package (2,214,648 bytes, 182 files), not a code change.
  I think the modifications were by Basemod.
