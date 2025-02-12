# Using Blender

<hr>

**Note that this document will not cover the basics of Blender.**

Several tools were created to make Blender compatible with modding Arc System Works games.

## ASW Modding Tools

A blender addon used by many when modding Strive, it simplifies the process of either extracting models for animation purposes or for modding purposes. Supports automatically creating & adding textures to the below custom material.

Install same as any blender addon. Clear Junk Materials deletes your outline material (for mesh modding), don't use it.

[Here's my fork](https://github.com/muuyo/CA_ASW_Tools/releases/tag/release)

[Doc on how to use it](https://docs.google.com/document/d/1m_h7p1WYypsvx2bpqFwvOS_aT1Vr_-jp5GQZK_X2dNA/edit?tab=t.0#heading=h.bxwyrhpezygq)

[backup ODT of above doc](files/ASWToolsGuide.odt)

## Aerthas' custom materials & shaders

[Download BLENDER-Arc-System-Works-Shader](https://github.com/Aerthas/BLENDER-Arc-System-Works-Shader)

While not strictly needed for modding, the shader is highly recommended for previewing models and textures within Blender itself.

Aerthas made a ton of practical videos on how to use his shader. [Here is a link to a playlist containing said videos](https://www.youtube.com/playlist?list=PLCkHUM_E60CSi1HowXR3v4uVWNqUDsl9l).

## Scripts

[Browse Arc-Sys-scripts](https://github.com/SaitsuP/Arc-Sys-scripts)

The most useful scripts have their own [wiki pages](https://github.com/SaitsuP/Arc-Sys-scripts/wiki), which also go into detail on how to use them.

## A note on Blender FBX export into UE4

You are going to need the modded FBX addon by Ryn for anything related to mesh exporting. It can be acquired [here.](../modding-mesh/io_scene_fbx_arcsys.zip)

When exporting with this, you first **need to set your armature's name to Armature**; else, your mesh will be completely invisible. For particle meshes (ones without armatures), this is avoidable.  
![texture settings](image-1.png)  
Select your mesh then your armature; then, export with these settings.  
![export settings](image-2.png)  
You may want to turn on Triangulate Faces. As well, if your Unit Scale (in your project) is not .01, change Scale to .01. You can save all these settings using the Operator Presets at the top.