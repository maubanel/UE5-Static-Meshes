<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Pivot Point

<sub>[previous](../lod/README.md#user-content-levels-of-detail-lod) • [home](../README.md#user-content-ue4-static-meshes)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

The pivot point of the model is where the movement widget is placed in UE5.  It is where you move the model to and from.  This is also the point of where the model is rotated from.  It is very important to the level designer that these are consistently placed and logically with how they need to snap to the level.  Any object that is supposed to snap to the group usually has its pivot point at the bottom center.  This is often ignored by the artist and good team communication is key on placing these correctly.

<br>

---


##### `Step 1.`\|`SUU&G`|:small_blue_diamond:

Go to the game and lets look at a bad pivot.  Lets move our pivot on the nanite column.  Change to **Modeling Mode** and select the column. Select the column to edit then **Tranform | Pivot** and you can change the location of the pivot.  Put it somewhere just outside the model then press the <kbc>Accept</kbd> button. What this does is moves where the transform gizmo is located.  So when you move the model it will be based from this pivot point. 

https://user-images.githubusercontent.com/5504953/129869570-9f543390-61f2-468c-bc69-3950d222574f.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

We can fix the pivot in two ways.  First we can do it in the editor. You can go into an orthographic view and press the <kbd>alt middle mouse button</kbd> and drag the pivot to the new position.  Now you right click on the pivot and select **Pivot | Set as Pivot Offset**.  The issue is that it is a bit buggy.  If I snap to the ground (<kbd>End</kbd> key) then the pivot resets.  Also if we add another copy of the mannequin to the level the pivot will be the incorrect one.  This really needs to be fixed in a 3-D authoring package like Maya.

https://user-images.githubusercontent.com/5504953/129871769-4b2a9863-6824-4a11-9b20-fcb37ad27aa2.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

"You want the pivot point to be where the object rotates and moves from.  Reimport [SM_SoloLSUGlove.fbx](../Assets/SM_SoloLSUGlove.fbx) into Maya. We cannot access the translation tools as these are locked in maya. Highlight the translation and rotation channels and right click and select **Unlock Selected**.  Now go to the **Move Tool** and **Rotate Tool** and see how it moves and rotates from this point.  Undo your changes so the rotation and translations are reset. 

https://user-images.githubusercontent.com/5504953/129874282-3bde86f7-29ce-4ec9-b87a-5b34b7470db1.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

It might make more sense to move the pivot point to the center of the wrist at the top of the model.  To do this in Maya press the **D** key to move the pivot in movement mode.  Zoom in and rotate around to confirm the placement.

https://user-images.githubusercontent.com/5504953/129876053-a04fa885-ce0e-46e3-a2ab-026c77875a93.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SUU&G`| :small_orange_diamond:

When it is correct, select the model and press **File | Game Exporter**. Now select the folder and the name of the file.  I called it in `SM_GlovePivot.fbx`. We not only have **Smoothing Groups** and **Trinagulate** selected but we also should **Move To Origin**.  Sometimes I find the pivot is not the same in Unreal and Maya unless this is selected.  The model is at origin so there should be no issues. Finally, press the **Export** button. 

![maya export settings](images/ExportSettings.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond:

Drag and drop this new **SM_GlovePivot** fbx into the **StaticMeshes** folder. Generate a collision and keep the other settings the same.  We will reuse the material we already created for the glove.

![import ](images/ImportFixedHand.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Assign the **M_Glove** material to **SM_GlovePivot** in the model viewer.

![alt_text](images/AssignGloveMat.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Drag the model in the game and notice the pivot point has changed but the rest of the model is intact.

https://user-images.githubusercontent.com/5504953/129878996-4da02739-b923-4da2-b39a-6c36de91c2cf.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

That's it for this lesson, **Save All** and submit to source control.  Push your final work to **GitHub**.

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`SUU&G`| :large_blue_diamond:

![save, commit and push to github](images/GitHub.jpg)

| `static.meshes`\|`THE END`| 
| :--- |
| **That's All Folks!** Thanks for sticking around. That's it for this lesson. |


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=The End!">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../lod/README.md#user-content-levels-of-detail-lod)| [home](../README.md#user-content-ue4-static-meshes) |
|---|---|
