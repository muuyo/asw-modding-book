# Functions of each texture
*This section was written by @muuyo*

<hr>
<br>

This page will detail the functions of each image in Strive:    
[here's a visualized version](https://docs.google.com/document/d/1ejZ9TrIFNwiawLcFj-XRtaO3Vg9TxD04sR8HKOaRkGI/edit) of this, i'll make gifs and fancy stuff later  

preliminary draft;

In this doc, when referring to values such as ".3", this usually means "30% white, mostly black" for instance. Different photo editors handle 30%/.3 differently.

## ColorXX (editable per color slot)  
- CHR_base is the base color of your character. the alpha of this image decides how shiny the material is.  
- CHR_Sss *is* the shadow color of your character - this game has no shadow color handling. The Alpha of this image defines *Taste* and *Asano* gradients, more specifically which parts of the image get them. 
  - Set this to .3 on a part to get the Asano gradient (usually used for hair).
  - Set this to .7 on a part to get the Taste color
  - These gradients are both set in the material, *not* any textures, so you almost always want this alpha completely black unless you are material instancing.
- CHR_decal is used for parts of the model that want a "transparent" texture to overlay onto the base. Very commonly used for small bits of text on models. Grey means transparent; anything lighter or darker becomes opaque.
- CHR_olm is only on some characters, and essentially defines how much of the SSS "bleeds" into the outline.
  - Completely black means black outlines. As you get brighter, the outline starts reflecting the color of the SSS. I believe full white on this actually glows.

## Base (only available per color slot using material instances)
- CHR_Detail is used for small lines, scrapes, folds, etc drawn onto the character. This is *overlaid onto Base*, whereas CHR_decal are seperate tiny bits of the model.
- CHR_ILM is a complicated texture; view the above doc for better info.
  - Basically, this texture *should be edited in Photoshop channels mode*. Each channel of this image (R,G,B,A) does different things entirely.
    - Red stores *how bright highlights are* - e.g. how bright the shiny part of shiny materials is.
    - Green defines when something becomes shaded.
      - < 0.1 on this makes something permanently very dark.
      - < 0.25 on this makes something permanently shaded.
      - 0.5 on this is the baseline, and is usually what you want.
      - 1 on this makes something *permanently unshaded*.
    - Blue is how powerful that part is highlighted. Keep this 0.5, but you can go darker or brighter to apply more "highlight" (e.g. parts become brighter) to random bits. (Better visual in above doc)
    - Alpha (edit this separately if you choose to) *manually draws outlines onto the model at that spot no matter what*; this is different from Detail in that OLM is applied, and this works entirely like normal outlines.