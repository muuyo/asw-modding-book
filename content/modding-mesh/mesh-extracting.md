# Extracting your mesh
*This section is under construction, and was written by @muuyo*

<hr>
<br>

You're looking to use either [Fmodel](../tools/fmodel.md), 
or [Umodel](../tools/umodel.md).
Learn how to set each up at the links above.
Umodel is a more antiquated piece of software; Fmodel is more recent, and I personally prefer using it. As well, it seems to currently be the only software that supports exporting material names, animations and every other asset! Umodel is mostly here for posterity.

<hr>

Either way, mesh locations you'll want to look for:

- Character meshes are stored in a tree like `RED\Chara\ANJ\Costume01\Mesh`
- Character meshes *used for moves* are stored in places like `RED\Chara\ANJ\Common\Effect\Particles\ANJ_PTC01\Mesh`. This is much more trial and error, however most are named after their [animation IDs, linked here.](https://docs.google.com/spreadsheets/d/1qrsX0QnmltX6DumfoRX7a76uvRJNh4AfU3QFdtOkcYc/edit?usp=sharing) Warning, these are shared across every color on that character, just like normal mesh mods.
- Map meshes are stored in `RED\Map\Battle\` under their internal name - an index is [linked here.](https://docs.google.com/spreadsheets/d/1qrsX0QnmltX6DumfoRX7a76uvRJNh4AfU3QFdtOkcYc/edit?usp=sharing). This is slightly outdated, but you should be able to figure it out.


<br>
<hr>

## Fmodel
Set up Fmodel using the tutorial [here](../tools/fmodel.md).

This is a newer method, however most likely much less of a pain to use, and more foolproof.
- Follow the steps on the [Fmodel page](..//tools/fmodel.md) to download and configure Fmodel and the Blender addon to accept .ueformat files
- Optionally, double click any file to preview it in Fmodel's viewer
- Right click any file in Fmodel, and export as a ueformat file as in the page linked in Step 1
<br>
<hr>

## Umodel
Set up Umodel using the tutorial [here](../tools/umodel.md).
- now, browse through the game's file trees to find whatever you wish to extract, then either right click the folder on the left and press Export folder content. **You want GLTF.**
- or, right click an individual file and do so. For more detailed overhaul-y mesh mods, I recommend exporting animations at this step as well, [explained in section 7,](../modding-animation/animation-intro.md) as having them in Blender will mean you don't have to extract the mesh again later - they're very useful for finding when and how your model **will** jank out.

<br>


After either method, view [the mesh importing section.](mesh-importing.md)