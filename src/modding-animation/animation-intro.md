<<<<<<< HEAD
## Animation intro
*This section is under construction, and was written by @muuyo*

<hr>
<br>

haven't written this yet but TLDR here's how ya do it in words

umodel: double click the model (e.g. pot_body), hit O to open the asset viewer, go to your animations (e.g. Costume01/Animation/default/body), select however many of those animations you want, hit the arrow beside Open -> add to loaded set, preview them in Umodel using spacebar and right/left bracket

to export, ctrl X and export em to a GLTF. animations will be in the same file
<hr>
for Fmodel, instead right click any animation in the path said above, hit "Save animation" (you usually want your exports set as `uemodel` in fmodel settings), then in Blender select the skeleton & use the ueformat addon to "import ueanim" and select that file

to swap between em, you want a Dope Sheet panel in blender, then swap it to Action Editor in the second dropdown; then change between them using the dropdown in the top middle of that panel. only works when the skeleton is selected.
=======
# Animations
*This section is under construction and was written by @bafrag*
<hr>
<br>

This section is all about animations. How to extract, edit and import in the game. To start you need those tools:
- The custom Unreal Engine from [section 1](ue4/getting-unreal.md)
- A copy of Blender
- A copy of Unreal Pak from the [pak section](packing/pack-intro.md)
- HeX editor (I suggest you to use 010 Editor)
- Fmodel from [section 3](tools/fmodel.md)
- AssetEditor from [section 3](tools/asseteditor.md)
>>>>>>> 666cd8a (Animation is done)
