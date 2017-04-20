[<- back to Character Workflow](CharacterWorkflow.md#5-export-the-character-daz3d)

# Import a Character into Unreal Engine 4

Totally easy because UDK supports the FBX file format :wink: We can simply import the just saved .fbx generated with Maya/Motion-Builder as a new Asset.

Important is to make sure the option "Sekeleton" is set to "None" - as you want to let UDK generate a Skeleton Asset for the imported character the first time. Also activate the checkbox "Import Animations" and choose there the option "Duration as Imported".

This way you will import the basic mesh of the character, his skeleton and all the animations for that skeleton and also all materials with their textures. This can take a while, on a complex Daz 3D character with an i7 4,2 GHz, 8 core and 32GB memory and a GTX 970 up to 15min easily.

## Tipps

### Skeleton

If you import a second character with the same skeleton and the same height - you can choose for the "Skeleton" the already existing Skeleton asset now. This makes it possible to re-use all the animation assets on any further character, using the same Skeleton asset :sunglasses:

`Behold! the new imported character which want to use the already existing skeleton asset must be in the same height! If the character is taller or smaller, the final output in the game will stretch/squeeze the mesh of the character as the bones of the skeleton asset are in the wrong length and can modify the whole mesh trough the skinning totally wrong then!`

### Materials

It's important to rework the just imported Material assets. The import mostly just understands the simple mapping of the basic color texture and maybe also the opacity channel.

The most dramatic effect can be achieved for the skin texture. UDK has an integrated "skin shader" which supports SSS (Sub-Surface-Scattering). So it is totally worth it to shortly google for a little tutorial how to build an SSS material (which is quite complex!).

You will find yourself in the situation that you miss many textures to fully achieve this -> the normal map, bump map, highlight map and sss-map itself. Nice is, Daz 3D supports SSS too :smile: So this means that most nice characters of Daz also comes with all those needed textures to achieve SSS, you just need to import them on your own! :sunglasses:

To do that -> open up the "Daz Install Manager" because in the UI of this little guy is a nice link to directly jump into the directory of all installed Daz 3D Assets (and character data). With an Explorer window open on that path, just search for an already known texture name of a skin-texture you have imported now. By finding the path of this one skin-texture, you also found the directory where all the other textures are stored for the other channels of SSS :wink:

Now take that path and import all those raw textures directly as assets into your UDK project and start using them in your new, shiny SSS material!

[UDK SSS Example](https://www.youtube.com/watch?v=Cl3yFu5KEvc)
