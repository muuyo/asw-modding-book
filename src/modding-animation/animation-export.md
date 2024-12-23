# Export Animation in the Unreal Engine
*This section is under construction and was written by @bafrag*
<hr>
<br>

## Blender
1. While holding Ctrl select first the model and then the Armature <div align="center"><img src="images/Ctrl-Select.png"></div><div align="center">
2. Export as FBX with these settings: <div align="center"><img src="images/Export-Settings.png"></div><div align="center">
3. The file name should match the .uasset file + add _mesh. anj000_body01_mesh in our case.

## Unreal Engine
1. Recreate the full folder path. "Chara\Costume01\Mesh", "Chara\Costume01\Animation\Default\body"
2. Press Import and import the .fbx file with these settings: <div align="center"><img src="images/UE4-Import-Settings.png"></div><div align="center">
3. After installing move the animation file to Chara\Costume01\Animation\Default\body folder and other to Mesh one.
4. Open Animation file and set Interpolation to Step <div align="center"><img src="images/Interpolation-Step.png"></div><div align="center">
5. Scroll down till you find Bone Compression Settings and copy it. <div align="center"><img src="images/Bone-Compression.png"></div><div align="center">
6. Create the Shared\AnimCompressMod path and paste here copied Bone Compression Settings <div align="center"><img src="images/AnimCompressMod.png"></div><div align="center">
7. Open the animation file again and choose the Bone Compression Settings from Shared\AnimCompressMod folder <div align="center"><img src="images/BoneCompressShared.png"></div><div align="center">
8. Make sure that every file is named correctly, save all and cook for Windows.
