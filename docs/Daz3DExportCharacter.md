[<- back to Character Workflow](CharacterWorkflow.md#5-export-the-character-daz3d)

# Export a Character in Daz3D

1. The default T-Pose of a Daz3D (Genesis 3) Character doesn't have straight arms..
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig19.jpg?raw=true" width="600"/>
</p>
_This will cause an invalid sekeleton definition in MotionBuilder afterwards, so we better fix this already in Daz3D._

2. We can easily fix this by selecting the forearm alone and rotate it in Y-axis ("Bending" it)
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig20.jpg?raw=true" width="400"/>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig21.jpg?raw=true" width="400"/>
</p>
_Just rotate it till we have straight line - it turned out this is exactly at value "16", depending on the side and bone + or -_

3. Do the same with the wrist/hand "Side-Side" value
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig22.jpg?raw=true" width="550"/>
</p>

4. Repeat this on the other side and then goto "File->Export"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig23.jpg?raw=true" width="200"/>
</p>

5. Choose "Autodesk FBX" as the output format, give it a name and press "Export"
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig24.jpg?raw=true" width="720"/>
</p>

6. A dialog appears with export options for .fbx format - the defaults are ok
<p>
  <img src="https://github.com/rocket-monkey/3d-howto/blob/master/docs/images/daz3d/fig25.jpg?raw=true" width="316"/>
</p>

7. Press "Accept" and you will have the character exported as .fbx file
