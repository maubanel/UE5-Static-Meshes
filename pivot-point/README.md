![](../images/line3.png)

### Pivot Point

<sub>[previous](../lod/README.md#user-content-levels-of-detail-lod) • [home](../README.md#user-content-ue4-static-meshes) • [next](../nanites-ii/README.md#user-content-nanites-ii)</sub>

![](../images/line3.png)

The pivot point of the model is where the movement widget is placed in UE5.  It is where you move the model to and from.  This is also the point of where the model is rotated from.  It is very important to the level designer that these are consistently placed and logically with how they need to snap to the level.  Any object that is supposed to snap to the group usually has its pivot point at the bottom center.  This is often ignored by the artist and good team communication is key on placing these correctly.

<br>

---


##### `Step 1.`\|`ITSM`|:small_blue_diamond:

Go to the game and lets look at a bad pivot.  Lets move our pivot on the nanite column.  Change to **Modeling Mode** and select the column. Select the column to edit then **Tranform | Pivot** and you can change the location of the pivot.  Put it somewhere just outside the model then press the <kbc>Accept</kbd> button. What this does is moves where the transform gizmo is located.  So when you move the model it will be based from this pivot point. 

https://user-images.githubusercontent.com/5504953/184548700-8993a7fb-c4aa-4e56-bc8a-b24d9dddf1d7.mp4

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

This also affects where the object will rotate from.  So when you switch to the **Rotation** gizmo the column will rotate from that point.  Clearly this is not a great spot to rotate this object around for placement.

https://user-images.githubusercontent.com/5504953/184548825-c9c6187b-fc66-4ff1-8a75-ef9fb808e638.mp4

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

We can also scale from this pivot point.  So the object will move to and from this point when scaling.  Again, strange to have it outside the model like this.

https://user-images.githubusercontent.com/5504953/184548936-6ece2990-7ce6-43e1-9f14-5317d86b6498.mp4

![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

You want the pivot point to be where the object rotates and moves from.  So if this object was a floating pickup then the center of the object would be a logical place.  In **Tranform | Pivot** you can press the <kbd>Center</kbd> button and set the pivot in the center.  

Now go to the **Move Tool**, **Rotate Tool** and **Scale Tool** and see how it moves and rotates from this point.  This would be good for free placement of objects in the X,Y,Z axis.

https://user-images.githubusercontent.com/5504953/184551359-5d703ac7-c2f6-4b8e-ad01-150c9dbb0f5f.mp4

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Now lets imagine you only wanted these columns in the corner of a room. These are columns on the ground so you would go to **Tranform | Pivot** you can press the <kbd>Bottom</kbd> as they are always on the ground and you might want to move the pivot to a corner for better corner placement.

https://user-images.githubusercontent.com/5504953/184551520-36610342-cdea-4072-a383-2332093e69d0.mp4

![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:

It might make more sense to move the pivot point to the center of bottom of the column as this will probably be placed around an outdoor setting and moved around on the X & Y axis.  So lets set the **Tranform | Pivot** to the <kbd>Bottom</kbd> button and leave it in the bottom center.  For this shape, this will be the best spot.  Notice this is the same spot that the creators of the statue model placed theirs!  Go ahead and make sure all the column models have the pivot in the bottom center.

![import ](images/ImportFixedHand.jpg)

![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Assign the **M_Glove** material to **SM_GlovePivot** in the model viewer.

![alt_text](images/AssignGloveMat.jpg)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Drag the model in the game and notice the pivot point has changed but the rest of the model is intact.

https://user-images.githubusercontent.com/5504953/129878996-4da02739-b923-4da2-b39a-6c36de91c2cf.mp4

![](../images/line2.png)

##### `Step 9.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

That's it for this lesson, **Save All** and submit to source control.  Push your final work to **GitHub**.

![alt_text](images/.jpg)

![](../images/line2.png)

##### `Step 10.`\|`ITSM`| :large_blue_diamond:

![save, commit and push to github](images/GitHub.jpg)

<!-- | `static.meshes`\|`THE END`| 
| :--- |
| **That's All Folks!** Thanks for sticking around. That's it for this lesson. | -->


![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE"> -->
![next up next tile](images/banner.png)

![](../images/line.png)

| [previous](../lod/README.md#user-content-levels-of-detail-lod)| [home](../README.md#user-content-ue4-static-meshes) | [next](../nanites-ii/README.md#user-content-nanites-ii)|
|---|---|---|
