[<- back to Character Workflow](CharacterWorkflow.md#6-bake-animations-to-the-character-motionbuilder)

# Bake Animations to Character in MotionBuilder

1. Repeat the steps from ["Load reference character and define skeleton"](LocomotionMB.md) but now with your Daz3D Character .fbx and with the skeleton template for Genesis 3.
_Select "Ignore All" when he complains about some axis invalidities_

2. In "Character Controls", click the drop-down "Source" and select "Control Rig", choose "FK/IK" in the upcoming dialog
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig20.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig21.jpg?raw=true" width="316"/>
</p>

3. Press the big blue button and select "File->Load Character Animation...", browse to the final locomotion .fbx we have created before with our mixamo package
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig22.jpg?raw=true" width="316"/>
</p>

4. Select "Plot to Control Rig" in the "Load Technique" radio selection and press "Open"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig23.jpg?raw=true" width="550"/>
</p>

5. Tada, your character starts to move! And you should see now all Takes in the Navigator, you can go trough them by double-click
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig24.jpg?raw=true" width="720"/>
</p>

5. Plot now every Animation/Take to the skeleton -> select a take by double-click, select "Source->Control Rig", press big-blue button and choose "Bake (Plot)->Bake (plot) To Skeleton"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig25.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig27.jpg?raw=true" width="316"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/motionbuilder/fig26.jpg?raw=true" width="316"/>
</p>

6. Repeat this with every Take and finally "File->Save As" to a new .fbx file -> we are almost done!
