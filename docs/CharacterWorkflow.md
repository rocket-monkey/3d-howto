# Character Workflow

How to build a character with [Daz3D](https://www.daz3d.com/), export it to [MotionBuilder](http://www.autodesk.com/products/motionbuilder/overview), bake [Mixamo](https://www.mixamo.com/) animations to the skeleton, take it over to [Maya](http://www.autodesk.de/products/maya/overview) for manual optimization and finally - export to [UnrealEngine 4](https://www.unrealengine.com/) where we can use the model together with the animations with a full game character "blueprint"

> For important files, there is a dropbox folder called "/Creativity/3d work" - check this one out for files in question!

## 1. Install Software

* Get [Daz3D](https://www.daz3d.com/) -> it's free, besides the assets-store
* Get [MotionBuilder](http://www.autodesk.com/products/motionbuilder/overview) -> look into the dropbox-folder
* Get [Maya](http://www.autodesk.de/products/maya/overview) -> look into the dropbox-folder
* Get an account at [Mixamo](https://www.mixamo.com/) -> it's free
* Get [UnrealEngine 4](https://www.unrealengine.com/) -> it's free

## 2. Create a Character (Daz3D)

Daz3D is a wonderful software for beginners. We don't need to have any modelling/texturing skills to generate wonderful human models. Daz3D is basically an extremely sophisticated character-generator, coming with a very detailed human body for male and female characters. We can customize the character by hundreds of different sliders and just paint it with pre-defined textures and clothings.

Everyone can create a nice humanoid character within minutes in this App! And because it is supportin .flv as export format, it fits perfectly into our 3D workflow together with MotionBuilder/Maya and UE4. Oh last but not least - the characters have a built-in skeleton in them, with a perfect skinning setup, ready to animate ;)

1. Set the layout to "Hollywood Blv."
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig01.jpg?raw=true" width="420"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig02.jpg?raw=true" width="180"/>
</p>
_it's the only layout of the UI where i know where all the tools are.._

2. Change to "Actors, Wardrobe & Props" activity, select "Figures"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig03.jpg?raw=true" width="273"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig04.jpg?raw=true" width="100"/>
</p>

3. Double-click e.g "Genesis 3 Male" to create a male character
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig05.jpg?raw=true" width="250"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig06.jpg?raw=true" width="400"/>
</p>

4. Customize the shape, select character and goto "Shaping" pane
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig07.jpg?raw=true" width="400"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig08.jpg?raw=true" width="320"/>
</p>
_change the shape by playing around with all different sliders - depending on the asset you are working with, these can be more or less sliders_

5. Customize the texture, select character and goto "Smart Content" pane, and select "Materials"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig09.jpg?raw=true" width="205"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig10.jpg?raw=true" width="350"/>
</p>
_just double-click any material you want to apply to the character. if you don't find something that matches your whish - you will end up buying new stuff in the store of daz3d.com. it's not that easy to build stuff from scratch regarding models and textures in daz3d, but the store is huge._

6. Select more important "Smart Content" with "Wardrobe" and "Hair" for your character
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig11.jpg?raw=true" width="350"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig12.jpg?raw=true" width="350"/>
</p>

7. Use "Surface Selection Tool" to select parts of the model, e.g. to delete an unwatned helmet from a wardrobe
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig13.jpg?raw=true" width="250"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig14.jpg?raw=true" width="250"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig15.jpg?raw=true" width="250"/>
</p>

8. Select parts and customize options for them, e.g. use "Smart Content" -> "Materials" for a selected "Hair" part
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig16.jpg?raw=true" width="250"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig18.jpg?raw=true" width="250"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig17.jpg?raw=true" width="250"/>
</p>

## 3. Get Animations (Mixamo)

Get a free account at mixamo.com and just surf around in their animation "store". Most of them are free and you can easily click-together a set of animations, also called a "Locomotion". A Locomotion is just a collection of multiple animation-loops, fitting a special need for a game for example. Maybe you want to just have a running, turning, crouching and jumping animation to build the real "Locomotion" afterwards in your game-engine -> e.g just everything needed to move around the character in the game-world. Then you can have another collection, another locomotion delivering everything needed to have a fight with an enemy (punches, defence-moves etc.).

## 4. Setup the "Locomotion" (MotionBuilder)

To make the mixamo animations usable with our workflow, we have to "convert" them into a MotionBuilder (MB) project file. We can do this by important the reference character of mixamo, defining the skeleton for it and baking all the mixamo original animations directly to this model. After we have saved this into a MB file, we can use this particular file afterwards as our "Locomotion" to import all of those animations into _any_ MB model we want to work with.

## 5. Export the Character (Daz3D)

We have to check the specific positioning of the whole character skeleton before we can savely export a Daz3D character to work with in MotionBuilder.

### 5.a Setup Skeleton for Genesis in MB

To proper work with a Genesis Character coming from Daz3D, we have to setup a "sekeleton-configuration" in MotionBuilder (MB) once. In this configuration, we're telling MB which bone is for which purpose - going trough every single bone and giving each a specific purpose in the skeleton table of MB. We can save this in a file for later usage so it's only needed to setup once. By having this possibility - we can work with _any_ character model from _any_ source, as far as the skeleton of it is somehow human and having all the minimal needed joints/purposes in it to bind with the MB table.

## 6. Bake Animations to the Character (MotionBuilder)

Import the Daz3D character model into MotionBuilder and bake our already created Locomotion onto it.

## 7. Final Optimizations (Maya)

We can rework the whole thing with Maya _as we want_ - Maya is the best in .flv exports and understands _all_ the parts of the model so far (mesh/bones/skinning/texture/animation). So we can customize everything to our liking here, like lower the poly-count, removing parts or even re-model parts of the mesh or refine the skinning. Even if you don't do anything like this, go trough Maya to create the final .flv in all cases so you'll never having problems in the final import into UE4.

## 8. Import to the Game (UnrealEngine 4)

TODO
