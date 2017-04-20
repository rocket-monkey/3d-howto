[<- back to Character Workflow](CharacterWorkflow.md#4-setup-the-locomotion-motionbuilder)

# Setup Locomotion in MotionBuilder

## Load reference character and define skeleton

1. Unpack the downloaded .zip file you got from mixamo.com - it should look like this
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig01.jpg?raw=true" width="316"/>
</p>

2. Open MotionBuilder and import the reference character by "File->Open"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig02.jpg?raw=true" width="420"/>
</p>
_Depending on the character you have chosen to work in mixamo, the name of the file for the reference character differs in the zip!_

3. Deselect the "Takes" in the Import-Dialog in the right pane
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig03.jpg?raw=true" width="420"/>
</p>
_As we only want to import the bare character first, without any animations - deselct all the Takes ;)_

4. Set "Display->X-Ray" to make the bones visible trough the model
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig04.jpg?raw=true" width="720"/>
</p>

5. Select the "Hip" Bone in the Navigator
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig05.jpg?raw=true" width="200"/>
</p>

5. Press the big "Skeleton" button underneath "Define" and select "Define" in the upcoming dialog
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig06.jpg?raw=true" width="550"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig07.jpg?raw=true" width="250"/>
</p>

6. Now we can define the skeleton, bone-by-bone - or we load the definition by a pre-defined template
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig08.jpg?raw=true" width="420"/>
</p>
_We can select bone-by-bone in the Navigator and then right-click the equivalent bone in the definition (in the right pane) and select "Assign bone". After we have done that with every bone in the character, we can save this definition as a template with the little save-button on top of the skeleton pane. Browse to the dropbox-folder/assets to lookup existing ones for Genesis 3 and Mixamo._

7. It can happen that the validation for the skeleton fails -> we get "yellow" bones in this case
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig09.jpg?raw=true" width="316"/>
</p>

8. Select the bone with the "Rotate" tool and rotate them in the axis in question till the validation turns green
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig10.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig11.jpg?raw=true" width="316"/>
</p>

9. When done, press "Lock Character" to finally "define" the skeleton and get the "Control Rig", select "Biped" in the upcoming dialog
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig12.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig13.jpg?raw=true" width="316"/>
</p>

## Import the animations as "Takes"

1. With the open reference character, goto "File->Motion File Import"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig14.jpg?raw=true" width="316"/>
</p>

2. Select all the animation files together, select "Merge" option in the import dialog in the radios left
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig15.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig16.jpg?raw=true" width="316"/>
</p>

3. Now you see how the character skeleton changes to match the animation!
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig17.jpg?raw=true" width="316"/>
</p>

4. Browse to "Takes" in the Navigator, double-click one to activate it
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig18.jpg?raw=true" width="316"/>
</p>

5. Now press "play" in the movie controls and toggle the "repeat" button, the one on the right of the movie controls
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig19.jpg?raw=true" width="500"/>
</p>

6. Rename the takes as you want, remove the ones you don't need and finally save this as a new .fbx file by "File->Save As"
_This final file will be used as a reference "locomotion" for further projects. The power of MotionBuilder is, that we can merge those animations to any character model as soon as the bones are configured with MotionBuilder's internal sekeleton definition._

# Update

it's not working this easy anymore, don't ask me why -.- What we need to change in the workflow to get it working again is:

* Create a control-rig before you import the motion-file. Achieve that by selecting "Control Rig" for "Source" on top-right in the UI - if there is none it will start the dialog to create one, just create it.

* Now in the middle-down of the UI, choose somewhere somehwat like "Control rig as skeleton input", i try to remember where and update here perfectly

* Now you can import the motion file as usual - and you must see a change in the stance so you know the animations applied correctly (what is the hard part after creating a control-rig that this works again..)

* After it worked this far, so you can click trough all the takes and you see the sekeleton AND the control-rig around it moving perfectly - then you're ready to save this baby with "Save as" and you have your working "Character Animation File" which can be imported as described in the next section onto ANY character.
