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