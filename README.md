# H4EK-FaceFXWrapper
A middleman tool which allows you to use the Dragon Age Origins toolset build of FaceFX with the Halo 4 & Halo 2 Anniversary Multiplayer Editing Kits to generate lipsync animations.


Please mind the gnarly text parsing code.
# Usage
1) Download the [Dragon Age Origins toolset](http://lvlt.bioware.cdn.ea.com/bioware/u/f/eagames/bioware/dragonage/toolset/DragonAgeToolset1.01Setup.exe)
2) Copy the contents of DragonAgeToolset\FaceFX to H3EK\bin\FaceFX
3) Rename FxStudio.exe to FxStudioOriginal.exe
4) Copy the H4EK-FaceFXWrapper files into your H4EK\bin\FaceFX folder (make sure this includes the bungie_facefx_actors folder!)
5) (Optional) Add a .txt file placed next to your sound file with the same name in the data folder, containing a read out of your voice lines for better lipsync generation
6) Import your sound using tool.exe with the import-lip-sync-data command. You must have a pre existing sound tag created for the function to work correctly e.g. for importing .wav files from data\sounds\dialog\test you must have a sound tag at tags\sounds\dialog\test.sound. data\sounds\dialog\test should be a folder containing all permutations of that sounds as .wav files.

# Limitations
- Tool cannot import more than 1024 curve keys, so the wrapper will only write the first 1024 to a FXX file. This should only be an issue for very long sounds (greater than a few minutes in length). Avoid using lengthy sounds for lipsync.
- Check the FaceFXWrapper.log file if you suspect there has been an issue with the lipsync generation.

# Advanced usage
- Use "FxStudio.exe -convertLTF <path>" to convert an LTF file to FXX
- Set the file paths in FaceFXWrapper.cfg to use a custom LTF or FXX file when importing a sound. This will override the FXX or LTF files used as long as the paths are set. Make sure to clear the config after use
