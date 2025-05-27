# Extracting Animation from the Game
*This section is under construction and was written by @bafrag*
<hr>
<br>

To extract animation from the game you'll need to use either [Fmodel for animation](tools/fmodel.md) or custom [Umodel](files/umodel_animscale.rar) for animation. That version prevents models to have scale issues (ASW loves use them in *every* character animation)

## Umodel
  1. After setting up Umodel go through game folders to character mesh file and open it.
  2. After that press "O" button.
  3. Then go to the animation folder Chara\ANJ\Costume01\Animation\Default\body (for example).
  4. Select **all** files, press "Open" -> "Append".
  5. By pressing brackets you can navigate through animations and by pressing Spacebar play them.
  6. Press either "Ctrl+X" or Export button to export .gltf file with animations.

## Fmodel
  1. Idk, muuyo, pls fill this section

You also need to save as .uasset files the animation files.
After extracting those files you can import them in Blender to edit them.
