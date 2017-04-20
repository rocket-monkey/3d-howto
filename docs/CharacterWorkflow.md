# Character Workflow

How to build a character with [Daz3D](https://www.daz3d.com/), export it to [MotionBuilder](http://www.autodesk.com/products/motionbuilder/overview), bake [Mixamo](https://www.mixamo.com/) animations to the skeleton, take it over to [Maya](http://www.autodesk.de/products/maya/overview) for manual optimization and finally - import to [UnrealEngine 4](https://www.unrealengine.com/) where we can use the model together with the animations with a full game character "blueprint"

> For important files, there is a dropbox folder called "/Creativity/3d work" - check this one out for files in question!

## 1. Install Software

* Get [Daz3D](https://www.daz3d.com/) -> it's free, besides the assets-store
* Get [MotionBuilder](http://www.autodesk.com/products/motionbuilder/overview) -> not free, look into the dropbox-folder
* Get [Maya](http://www.autodesk.de/products/maya/overview) -> not free, look into the dropbox-folder
* Get an account at [Mixamo](https://www.mixamo.com/) -> it's free but you need an Adobe ID
* Get [UnrealEngine 4](https://www.unrealengine.com/) -> it's free but you must register

## 2. Create a Character (Daz3D)

Daz3D is a wonderful software for beginners. We don't need to have any modelling/texturing skills to generate wonderful human models. Daz3D is basically an extremely sophisticated character-generator, coming with a very detailed human body for male and female characters. We can customize the character by hundreds of different sliders and just paint it with pre-defined textures and clothings.

Everyone can create a nice humanoid character within minutes in this App! And because it is supporting .fbx as export format, it fits perfectly into our 3D workflow together with MotionBuilder/Maya and UE4. Oh last but not least - the characters have a built-in skeleton in them, with a perfect skinning setup, ready to animate ;)

> 1. Only true downside i found in my journeys - the skinning of the latest "Genesis 3" human model is using "qubic-bezier" as skinning method. This produces very nice results tough, but the support of this method is only given in the latest 3d programs like Maya/3ds max. The support of this method in game engines is a different story, because the calculation of "qubic-bezier" is heavier compared to existing methods. Unity and UE4 are _not_ supporting it - the only one i found (no surprise) which _would_ is Cryengine :tada:. I tried to stick a character setup together with Cryengine too after i licensed it trough Steam - but i already failed completely at the very first screen of the setup wizard, even _with_ tutorials -.-

> 2. You ask yourself what is the downside of an engine, not supporting "qubic-bezier" as skinning method? Well, the skinning in a 3d character defines how the bones, while moving in an animation, will deform the surrounding mesh of the character model itself - what is especially needed around joints like an elbow or a knee. The skinning itself is just a texture with a painting on it, normally using just a simple gradient color-code going from somewhat green to red for example or just from black to white, defining where the skinning method is used "most" and "least" - you just paint this accuratly everywhere needed until the deformation of the "flesh" looks real (enough). Now, the skinning method is an algorithm in its core, processing the actual mesh (geometry/polygons) during an actual deformation which is triggered by the movement of the bones. It is moving the actual polygons in their places where they should be - so it is clear that the usage of different algorithms will give a different deformation result in the geometry. Now if an engine is not supporting a given method/algorithm, it will just fallback to one it actually supports -> resulting in totally different "looks". So you don't need to wonder why your Daz character is just not looking the same during an animation like it did in Daz or MotionBuilder or Maya. You can check this in Maya where you can select the skeleton and just change the skinning method from "qubic-bezier" to "basic" and you will see what happens afterwards in UE4/Unity with it. Now by knowing that, you could give yourself the pain-in-the-ass job and try to fix the deformations using the "basic" method in Maya - but this is an extremely advanced operation and even if you're skilled, still extremely time-consuming. You won't do it...

[Create a Character in Daz3D](Daz3DCreateCharacter.md)

## 3. Get Animations (Mixamo)

Get a free account at mixamo.com and just surf around in their animation "store". Most of them are free and you can easily click-together a set of animations, also called a "Locomotion". A Locomotion is just a collection of multiple animation-loops, fitting a special need for a game for example. Maybe you want to just have a running, turning, crouching and jumping animation to build the real "Locomotion" afterwards in your game-engine -> e.g just everything needed to move around the character in the game-world. Then you can have another collection, another locomotion delivering everything needed to have a fight with an enemy (punches, defence-moves etc.).

[Howto Mixamo](HowtoMixamo.md)

## 4. Setup the "Locomotion" (MotionBuilder)

To make the mixamo animations usable with our workflow, we have to "convert" them into a MotionBuilder (MB) project file. Well it's again just an .fbx file but with much more meta-data in it. We can achieve this by importing the reference character of mixamo, defining the skeleton for it and baking all the mixamo original animations directly to this model. After we have saved this into an .fbx file, we can use this particular file afterwards as our "Locomotion" to import all of those animations into _any_ character model we want to work with in MotionBuilder.

[Setup Locomotion in MotionBuilder](LocomotionMB.md)

## 5. Export the Character (Daz3D)

We have to check the specific positioning of the whole character skeleton before we can savely export a Daz3D character to work with in MotionBuilder.

[Properly export a Character in Daz3D](Daz3DExportCharacter.md)

## 6. Bake Animations to the Character (MotionBuilder)

Import the Daz3D character model into MotionBuilder and bake our already created Locomotion onto it.

[Bake Animations to Character in MotionBuilder](BakeAnimationsMB.md)

## 7. Final Optimizations (Maya)

We can rework the whole thing with Maya _as we want_ - Maya is the best in .fbx exports and understands _all_ the parts of the model so far (mesh/bones/skinning/texture/animation). So we can customize everything to our liking here, like lower the poly-count, removing parts or even re-model parts of the mesh or refine the skinning. Even if you don't do anything like this, go trough Maya to create the final .fbx in all cases so you'll never having problems in the final import into UE4.

[Finalize a Character in Maya](FinalizeCharacterMaya.md)

## 8. Import to the Game (UnrealEngine 4)

Now this is really easy after all the lengthy steps before :wink: Well, if you tried to achieve all this on your own, this step can feel like the hardest pain-in-the-ass because you always wait a few minutes to see how you failed with something. But in all the failed cases it's not the fault of UDK itself - the error is already there in .fbx file you want to import. So after going trough all the steps before without any problems, you should be fine and it will _just_ work!

[Import a Character into Unreal Engine 4](ImportCharacterUE4.md)
