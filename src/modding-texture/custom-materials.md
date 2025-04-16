# Custom materials
*this section was written by @muuyo*


A more comprehensive guide lies [here](https://docs.google.com/document/d/1hJ8L2PiS3xiPDKPt8q3sWQ9J6nzxlfnHOCggPh8jVOg/edit?tab=t.0), however **it recommends Lean's materials - do not use its M_CharaBase, use the one included with your custom editor!**

Also, **turn Share Material Shader Code off in Project Settings!**

<hr>

## Material instancing
Here's a small, easy place to start.
Materials in these games are very powerful. In Strive, even being able to edit the values that Arcsys program into them lets you do pretty interesting things;  
add gradients to your characters, make things glow, make recolors **work on Color13+**, and even use the special filter that Color16 skins have.  
Setting this up may be initially a little confusing. However, once you get it down, they're intuitive, easy to work with and preview (e.g. you can preview the recolor you're doing without ever booting Strive), and are a good branching point to custom materials (a much more technical process, however an incredibly powerful one)

So! To start, you'll need to instance  
TODO

<hr>
When written, this'll be a permanently-in-progress doc on how to make custom materials (including working with the M_CharaBase from Ryn's material recreations, which should come with your custom editor).
As materials are a pretty wide and well-documented field, I won't attempt to go over anything comprehensively, especially considering that materials work nearly exactly the same here as they do in normal Unreal.

In brief, though, materials in Unreal are basically math with colors, and UVs define where those colors go. That's it.
Place down a texture and it by default uses the UV from your model, but there's many more UVs you can feed into this - you will likely be looking for "ScreenPosition", which means the texture is essentially just static on screen as the model moves around.
If you were to, for example, feed that into a Panner node, you can now make a scrolling texture.
