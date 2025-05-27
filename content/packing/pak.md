# Creating a .pak archive


You're going to need UnrealPak to do this section. Download it here; [UnrealPak](../tools/files/Unreal_Pak.rar)

If you would rather a video overview, see below;
<video controls src="2025-04-01 15-56-33.mp4" title="unrealpak thing"></video>

First: the prerequisites. In order to package your mod, the folder hierarchy must follow the rule of `ModName\RED\Content\`, with the rest of the hierarchy matching the asset's original path.

As an example, if I am modding the asset sol_body in folder `RED\Content\Chara\SOL\Costume01\Mesh` and the mod is named LabcoatSol, I would:   
- take my cooked files from my cooking directory; this is in `/[ProjectName]/Saved/Cooked/WindowsNoEditor/[ProjectName]`.
- make a few folders in my UnrealPak directory; specifically, you want `(UnrealPak)/ModName/RED/`
- copy Content from your cooking directory into there, so your directory tree looks like `(UnrealPak)/ModName/RED/Content/Chara...`

Actually packaging your mod is quite simple: simply drag the mod folder onto the `UnrealPak-With-Compression.bat` file. It should spit out a file with the same name as the mod folder, but with the .pak extension.

Now, you can use this as a mod.
More detail on the [installing page](../packing/installing.md).