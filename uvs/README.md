![](../images/line3.png)
### UVs

<sub>[previous](../collisions/README.md#user-content-collisions) • [home](../README.md#user-content-ue5-intro-to-static-meshes) • [next](../nanites/README.md#user-content-nanites)</sub>

![](../images/line3.png)

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

[UV Mapping](https://en.wikipedia.org/wiki/UV_mapping) is a method of project a 2-dimensional texture on the surface of a 3-d model.  This can be for a texture color, the reflective qualities of an area on the surface or many other shader related topics.  The **U** and the **V** denote the X & Y axis of the 2D texture because **X**, **Y** and **Z** are used by the verticese in the 3-D model.  So **U** is the horizontal axis and **Z** is the vertical axis of the 2-D texture.

<br>

---


##### `Step 1.`\|`ITSM`|:small_blue_diamond:

Now go back to modeling mode and select **UVs | Layout**.  Now what this shows is a square texture with an exploded view of the polygons of the faces of the individual pieces were before they were combined.  So each pixel in this texture maps relates to a face in the model. 

![uv map viewer](images/uvMap.png)

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

So first lets try **UVs | Auto UV**. Make sure **Material Mode** is set to `Checkerboard`. Play around with the settings.  What we want to see is 1 meter squares evenly spaced.  No matter what I change I can't seem to get a clean uv map with the auto uv setting.

![auto uv poor results](images/uv0.png)

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Lets try unwrapping where the engine will try and unwrap the model to create a good UV map.  Again, I do not get any desired results.  In fact it is worse I have no texture at all on the top portion of the model.

![unwrapping](images/unwrapping.png)

![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now our final attempt is to project the UV's onto the closest shape.  Now since this is still cylindrical, select **Projection Type** and then select `Cylindrical`.  Press the <kbd>Accept</kbd> button.

![project UV's](images/projectModel.png)

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Now go back to **UVs | Auto UV** and it looks a bit better.  I can see some shapes that are not visible, like the top of the old cylinder.  I should have done a beter job cutting and discarding unused model before we merged the geometry. 

![new uv map](images/newUVMap.png)

![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:

Press **File | Save All** to save all your work to date.  There is a new plugin tool that we can use to edit UV's as well.  Go to **Edit | Plugins** and search for **UV Editor**. There will be a disclaimer about the tool not being final and you will need to restart the game.

![install UV Editor plugin](images/newPlugin.png)

![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now select the column in the game engine and select **Actor | Asset Tools | UV Editor**.

![select UV Editor from the Actor menu](images/uvEditorLoad.png)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

So you now see your UV's and they can be edited if you like.

![uv editor](images/uvEditorLoad.png)

![](../images/line2.png)

##### `Step 9.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/unwrapModel.png)

![](../images/line2.png)

##### `Step 10.`\|`ITSM`| :large_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 11.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: 

![alt_text](images/.png)

![](../images/line2.png)


##### `Step 12.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

![alt_text](images/.png)

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

| [previous](../collisions/README.md#user-content-collisions)| [home](../README.md#user-content-ue5-intro-to-static-meshes) | [next](../nanites/README.md#user-content-nanites)|
|---|---|---|
