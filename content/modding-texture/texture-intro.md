# Texture introduction
*This section was written by @muuyo*

<hr>
<br>

This is the basic layer of all modding in Arcsys games - recolors! You may wish to expand to mesh modding later, but this is usually what people go to first - and so will be a bit more comprehensive.

<hr>

First, the basic overview;
- Extract the game assets to somewhere on your computer using Fmodel; I usually just export all textures from my desired character's `Content/Chara/CHR/Costume01/Material` folder. **This should be in TGA;** you need information saved in the alpha channel. In Fmodel, you can set the export format to TGA under Settings.
- Open the textures for your color slot **in Photoshop or Photopea** (you almost always **need** separate alpha editing support)
  - These will usually be in:
    - Content
      - Chara
        - Character ID (e.g. SOL)
          - Costume01
            - Material
              - Base
                - CHR_ILM, which is used for material properties - reflectiveness, drawn-on outlines, etc
                - CHR_detail, which is used for little scrapes or folds drawn onto the character
              - ColorXX
                - CHR_base, which is the main color
                - CHR_Sss, which is the texture *used for shadows* - the game has no builtin "shadows" beyond this image
                - CHR_Decal, which is used for "transparent" overlays onto the mesh that require transparency, per-color variance or color
                - An assortment of other textures; CHRW_Base is the base for the Weapon, others are usually self explanatory.
  
- Now that you have your character's textures in Photoshop, you can begin editing them. I would recommend viewing the section [for previewing textures in Blender.](./texture-blender-preview.md) As well, you may want to view the [images page](texture-images.md) for a more detailed view on the operations of each texture.
- Once you have your textures edited to a desired goal, you can export them **as PSD or TGA** with 32-bit color and Compression On for the latter. Take care as to the alpha layers, in the images section.
- Then, simply pack them for Strive (or other Arcsys games) by following the [Exporting section.](../ue4/unreal-exporting.md)