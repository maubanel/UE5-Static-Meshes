![](../images/line3.png)
### Basic Column IV

<sub>[previous](../basic-column-iii/README.md#user-content-basic-column-iii) • [home](../README.md#user-content-ue5-intro-to-static-meshes) • [next](../pivot-point/README.md#user-content-pivot-point)</sub>

![](../images/line3.png)

Lets complete the pillar by adding a final piece on top that would support a beam so it can lie flat.

<br>

---


##### `Step 1.`\|`ITSM`|:small_blue_diamond:

Now lets create the box on top of the column that supports the ceiling/beam.  Go to the **Top** view and make sure you are in **Wireframe** render mode and select a size that works best for you. Pick a **Shapes | Box** tool with a **Width** and **Depth** of `130` and a **Height** of `30`.  Make sure **Align to Normal** is set to `false`. This is just larger that the top ring which is what I am looking for.

![select box and add shape](images/drawBoxOnTop.png)

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

Now left click to place the mesh and save it in **Meshes** as `DeleteMe`.

![save as delete me](images/saveDM.png)

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Lets remove the top of the column as we need to cut a hole to join with the box on top.  Select the **TriModel | TriSel** tool and pick a **Brush** of a small size and select all the triangles on the top of the column.  Press the <kbd>Delete</kbd> button. This will remove this top face.  When you are happy that you have done it correctly press the <kbd>Accept</kbd> button.

![remove top of column](images/removeTopOfColumn.png)

![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now I want to have rounded corners on this box.  We can do this by adding 4 edge loops to the shape.  The further the edge loop is away from the corner the greater the rounding of the corner.  The closer the less rounding happens on the edge.  So go to **PolyEd** and select the <kbd>Insert Edge Loop </kbd>button.  Add them with the large rounded area at the bottom.  It should look like the image below...

When you are happy press the <kbd>Accept</kbd> button.

https://github.com/maubanel/UE5-Static-Meshes/assets/5504953/1ff4e02a-473b-4b66-8659-0a237e334626

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Now this is where the magic happens. Select the **SubDiv** (Sub Division) tool and in **Wireframe** mode select how many subdivisions you want.  I set my **Subdivision Level** to `3`.  Look at the image as a lit perspective and you will see that all the edges are now rounded based on the location of your edge loops. When you are happy press the <kbd>Accept</kbd> button.

https://github.com/maubanel/UE5-Static-Meshes/assets/5504953/0601859f-6e4b-4363-85a4-22514fa039c7

![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:

Move the new rounded box to the top of the column and **Align** it on the **X** and **Y** axis so they are perfectly centered. Press the <kbd>Accept</kbd> button. For some reason this did not work for my model so I had to do it manually by eye.

![align top](images/alignTop.png)


![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now we will place the bottom of the new box so it is just a single unit below the top of the column so we can cut a hole in the top piece.

![place box just below column](images/justBelowColumn.png)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Make sure the column is centered and buttressed right next to the top cube.  Select the column then the top box and go to **PolyModel | MeshBool** and subtract B from A. Make sure you keep your inputs and press the <kbd>Accept</kbd> button.  You should notice inside that you have no stray polygons.

![cut hole in box](images/cutHoleBox.png)

![](../images/line2.png)

##### `Step 9.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now we will perform our final merge and clean up the materials so there is one slot with one color.

![final mesh merge and select one material](images/lastMerge.png)

![](../images/line2.png)

##### `Step 10.`\|`ITSM`| :large_blue_diamond:

That is it for the base modeling.  We could have done so much more but we have looked at many of the common and useful tools in UE5's modeling package so I think this is good start.  Next up lets look at it as an interactive model in the game.

![final column](images/finalColumn.png)

![](../images/line2.png)

##### `Step 11.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: 

Go to your **Meshes** folder and delete the scratch files that you no longer need (named delete).

![delete scratch files](images/cleanUpMeshes.png)

![](../images/line2.png)


##### `Step 12.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Now when Unreal saves a model it adds a hash number at the end.  Go to **Meshes** and rename your column to just `sm_column` and remove the suffix to the file name.

![rename hashed file](images/renameHashedFile.png)

![](../images/line2.png)

##### `Step 13.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Select the **File | Save All** then press the <kbd>Revision Control</kbd> button and select **Submit Content**.  If you are prompted, select **Check Out** for all items that are not checked out of source control. Update the **Changelist Description** message and with the latest changes. Make sure all the files are correct and press the <kbd>Submit</kbd> button. A confirmation will pop up on the bottom right with a message about a changelist was submitted with a commit number.

![save all and submit to perforce](images/submitP4.png)

![](../images/line2.png)

##### `Step 14.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Sometimes not all files get submitted to Unreal especially for files that don't show up in the editor.  It is good practice one you submit in **Unreal** and quit the game to right click on the top most project folder and select **Reconcile Offline Work...**.

This will either give a message saying ther is nothing to reconcile or bring up a tab.  Make sure that these are **NOT** files in the **Intermediate** and **Saved** folders as these should be ignored from the `.p4ignore`.

If the files are in **Content** or **Configuration** then press the <kbd>Reconcile</kbd> button.  Then submit the changes with a message and press the <kbd>Submit</kbd> button. In this case the megascan files did not get added when submitting through the engine interface.

![save all and submit to perforce](images/reconcileP4.png)

![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - Pivot Point"> -->

![next up pivot point](images/banner.png)

![](../images/line.png)

| [previous](../basic-column-iii/README.md#user-content-basic-column-iii)| [home](../README.md#user-content-ue5-intro-to-static-meshes) | [next](../pivot-point/README.md#user-content-pivot-point)|
|---|---|---|