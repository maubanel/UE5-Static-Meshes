![](../images/line3.png)
### Basic Column II

<sub>[previous](../basic-column/README.md#user-content-basic-column) • [home](../README.md#user-content-ue4-static-meshes) • [next](../)</sub>

![](../images/line3.png)

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Lets finish off the flutes and the top and bottom support for the column.  Lets also pick a nice material that we can use to finish it off.

<br>

---


##### `Step 1.`\|`ITSM`|:small_blue_diamond:

Now rotate the main column to cut 18 more holes at 18° each.  Rotate to `36`°, `54`°,`72`°, `90`°, `108`°, `126`°, `144`°, `162`°, `180`°, `198`°, `216`°, `234`°, `252`°, `270`°, `288`°, `306`°, `324`°, and `342`°.  Then do a boolean to cut out the shape 18 more times.               

https://user-images.githubusercontent.com/5504953/183221393-719dace0-27b3-4522-b98e-46a69a1ddbea.mp4

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

Now we can get acess to a plethera of free assets for our student projects at **Quixel**.  Open up the **Add Content** button and select **Quixel Bridge**.

![open up Quixel](images/quixel.png)

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now login with your **Unreal** credentials and select **Surfaces**.  Pick a solid surface that is fairly large (minimum 2m x 2m). I liked **White Cracked Wall**. I selected **Medium Quality** which is a **2K** texture (2048 x 2048) which is large enough.  Press the <kbd>Download</kbd> button which will get it onto your hard drive.  Then to add it to your project press the <kbd>Add</kbd> button.

![download quixe surface and add to project](images/whiteCrackedWall.png)

![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

This now adds a **Megascans | Surfaces | White Cracked Wall** folder to your project's **Content Browswer**.

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Assign `MI_Cracked_Wall` as a material to our **SM_Column** static mesh. Then double click the **MI_Cracked_Wall** material instance and set **Tiling Offset** to `true`.  Then adust the **Tiling X** and *Tiling Y** to match the scale.  I like a value of `5.0`.

![alt_text](images/adjustMaterial.png)

![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:

Now we do not need the small column anymore as we have used it.  Go to the **Meshes** folder and right click on **DeleteMe** and delete this static mesh.

![delete delte me file](images/deleteFlute.png)

![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now lets add a bottom to the pillar.  Make sure you are in **Modeling Mode** and select **Shape | Cyl**.  Set the **Radius** to `81.0` cm, **Height** to `10.0` cm, **Radial Slices** to `20.0` and finaly **Height Subdivisions** to `1`.

![add 81cm bottom cylinder](images/newBottomPillar.png)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now press the left mouse button to place it in the level.  It will bring up the static mesh prompt to save it.  Select the **Meshes** folder then call it `DeleteMe`. Press the <kbd>Save</kbd> button. 

Now this may not work as it might say this name is in use.  If it does you need to right click on **Meshes** and select **Fix Up Redirectors** (CHECK THIS).  Then try saving again. 

Once it is done, press the <kbd>Complete</kbd> button (if another save menu pops up press cancel).

![save mesh as delete me](images/saveTempDelete.png)

![](../images/line2.png)

##### `Step 9.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now select both the main column and this new bottom plate you have made.  Select **Transform | Align**.  Now we want to center it on the X and Y axis so set the **Axis | Align X** and **Axis | Align Y** to `true`.  Turn off **Align Z**. Now move the piece so that it fits over the column without a gap.  Press the <kbd>Accept</kbd> button.

![center bottom piece using align tools on x and y axis](images/alignCenter.png)

![](../images/line2.png)

##### `Step 10.`\|`ITSM`| :large_blue_diamond:

We are going to create a slant in the disc.  Go to the **Deform | Lattice** tool and set **Z Axis Resolution** to `2`.  Now left click and select all th points on the top of the mesh.  Triple check that you selected all of them and none of the ones below.

![select all top points in latice tool](images/latice.png)

![](../images/line2.png)

##### `Step 11.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: 

Now you can bring in the scale on both X & Y axis to tilt the top edge inwards. When you are happy press the <kbd>Accept</kbd> button.

![tilt top shape](images/adjustScale.png)

![](../images/line2.png)


##### `Step 12.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Now make sure the bottom ring is colliding with the cylinder.  

![alt_text](images/meshMerge.png)

![](../images/line2.png)

##### `Step 13.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 14.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 15.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 16.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 17.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 18.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 19.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 20.`\|`ITSM`| :large_blue_diamond: :large_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 21.`\|`ITSM`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)


![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE"> -->
![next up next tile](images/banner.png)

![](../images/line.png)

| [previous](../basic-column/README.md#user-content-basic-column)| [home](../README.md#user-content-ue4-static-meshes) | [next](../)|
|---|---|---|
