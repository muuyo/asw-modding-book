# Mesh troubleshooting
*This section is under construction, and was written by @muuyo*

<hr>
<br>
This section is where people have the most trouble, and so will likely be very long.  
The below sections are dropdowns.
<hr>
<details><summary><b>Models looking "dehydrated", or just generally really outwardly jagged and weird</b></summary>

The dehydration is, almost always, an issue of the armature applied to your model being incorrectly scaled for one of a variety of reasons. However, the remedy is generally the same:

- Verify that the unit scale in Blender (under the Properties window, look for the cone tab) is 0.01. **This is important!** As well, make sure you're using meters.

- Reimport the *source of your skeleton* - either from a GLTF from umodel, or a uemodel from Fmodel.

- Delete the model from this import, as you won't need it; click the skeleton, and hit N to bring up the Viewport sidebar. Under Item, **make sure it's a "normal" size**; e.g. 2.2 meters, and not 0.022 or 220.

- If you need to, scale up your model to match the size of the armature that you just imported. Hit S, then type 100 to scale it up by 100x, for example.

- Select your mesh, then select the new skeleton by control-clicking it, and hit ctrl P then Parent with All Transforms.

- Now, rename this new armature to Armature as standard, and use it as your new base.

If it's instead jagged and explodey, as best I can put it, it's a very similar issue - go into the armature's Edit or Pose modes and make sure the bones line up with your model. If not, set the Location (under the same sidebar) to 0/0/0 on the Armature, do the same to the Model, and move the model to where it needs to be in order to line up with the Armature.
</details>
<hr>

<details><summary><b>"These bones are missing from the bind pose" in UE4</b></summary>

You almost certainly have "Add Leaf Bones" on in your Blender model export settings. Please check the [Blender page](../tools/blender.md) for the correct export settings. You can save these as an Operator Preset so you don't have to redo it every time. 

</details>
<hr>
<details><summary><b> </b></summary>
</details>