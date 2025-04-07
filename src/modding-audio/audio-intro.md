# Audio

*this section was written by @muuyo*
<hr>

So! Audio.  
Long story short, the process essentially goes "save uassets using fmodel -> convert them to audio using the batch -> done"
Adding audio as a mod is pretty simple; put a **wav file** in the matching place in your Unreal project, then cook as normal.

So;
- Install Fmodel using [its guide](../tools/fmodel.md)
- Browse to where the assets you want are (usually something like `Content/Chara/XXX/Common/Audio/Voice`)
- right click the folder with all the assets you want to save (each asset is a sound file, usually easiest to do the whole language folder)
- Export Folder Package's Raw Data (uasset)
- Drop [this zip file](./UmodelSaved.zip)'s contents into wherever you extracted them (click the underlined text at the bottom to navigate there)
- The contents of this zip do a few things:
  -  ExtractAudio loops through all folders inside the current folder, and converts assets to .oggs (putting them in the same place)
  -  deluasset and deluexp delete all of their respective files after you're done; just clears up clutter.
-  Now, simply run "ExtractAudio" and all the files get converted.
-  [This google sheet](https://docs.google.com/spreadsheets/d/1qrsX0QnmltX6DumfoRX7a76uvRJNh4AfU3QFdtOkcYc/edit) may be helpful for figuring out which file is which; each sound file usually has an animation ID in its name, that would correspond to these.