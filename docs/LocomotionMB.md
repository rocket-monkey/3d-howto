[<- back to Character Workflow](CharacterWorkflow.md#4-setup-the-locomotion-motionbuilder)

# Setup Locomotion in MotionBuilder

1. Unpack the downloaded .zip file you got from mixamo.com - it should look like this
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig01.jpg?raw=true" width="316"/>
</p>

2. Open MotionBuilder and import the reference character by "File->Open"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig02.jpg?raw=true" width="316"/>
</p>
_Depending on the character you have chosen to work in mixamo, the name of the file for the reference character differs in the zip!_

3. Deselect the "Takes" in the Import-Dialog in the right pane
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig03.jpg?raw=true" width="316"/>
</p>
_As we only want to import the bare character first, without any animations - deselct all the Takes ;)_

4. Set "Display->X-Ray" to make the bones visible trough the model
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig04.jpg?raw=true" width="316"/>
</p>

5. Select the "Hip" Bone in the File-Browser
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig05.jpg?raw=true" width="316"/>
</p>

5. Press the big "Skeleton" button underneath "Define" and select "Define" in the upcoming dialog
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig06.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig07.jpg?raw=true" width="316"/>
</p>

6. Now we can define the skeleton, bone-by-bone - or we load the definition by a pre-defined template
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig08.jpg?raw=true" width="316"/>
</p>
_We can select bone-by-bone in the file browser and then right-click the equivalent bone in the definition (in the right pane) and select "Assign bone". After we have done that with every bone in the character, we can save this definition as a template with the little save-button on top of the skeleton pane. Browse to the dropbox-folder/assets to lookup existing ones for Genesis 3 and Mixamo._

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
