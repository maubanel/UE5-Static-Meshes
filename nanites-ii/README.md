![](../images/line3.png)
### Nanites II

<sub>[previous](../nanites/README.md#user-content-nanites) • [home](../README.md#user-content-ue5-intro-to-static-meshes) • [next](../)</sub>

![](../images/line3.png)

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

We have looked at the size of nanites and their advantages.  Lets look at performance.

<br>

---


##### `Step 1.`\|`ITSM`|:small_blue_diamond:

Right click on **Content | Level | Experimental** and select **Duplicate**.  Call this new level `Nanite Statues`.  Open up the new level and delete the two columns and two statues as well as the text on top of it so we just have the landscape.

![duplicate level and delete actors in scene](images/duplicateAndDel.png)

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

Drag the original **SM_Decorative_Statue_Pillar** nanite into the level.  Duplicate it and fill a large area up.  I put around 288 copies of the model which would be 288,000,000 triangles (288 million) as each model has ~1,000,000 triangles.  Make sure you **Player Start** is not inside a statue.  Press the three lines to the left of **Lit** and select `Show FPS`.

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Run around and you will see the framerate.

https://user-images.githubusercontent.com/5504953/184535866-12079a17-074d-4eee-b92e-9c2b06b78273.mp4

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Right click on **Content | Levels | Nanite Statues** and select **Duplicate** it and call it `NonNaniteStatues`.  Open up this new level by double clicking on it.

![duplicate and create nonnanitestatues level](images/nonNaniteStatues.png)

![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

In the **World Outliner** select all the statues in the level. Now we can edit the **Details** panel and change the **Static Mesh** to `SM_Decorative_Statue_Pillar_NoNan`.

![cchange all statues static mesh to SM_Decorative_Statue_Pillar_NoNan](images/switchModels.png)

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Now *press* the <kbd>Play</kbd> button in the top menu bar to launch the game. Now the framerate in my case is about half of what it was when using **Nanites**.

https://user-images.githubusercontent.com/5504953/184536436-a44a3fbd-2da3-4d28-a873-f2ac4107459f.mp4

![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:

So how did we create details before when we didn't have nanites (or when we can't use nanites like models with transparency or animated characters)? 

We use a [UV](https://en.wikipedia.org/wiki/UV_mapping) map, which assigns pixels in the image to a face on the model. So this is what a sphere would look like with a map texture applied to the UVs. A UV map is an unwrapped 2-D version of a 3-D Model.  This allows the renderer to know what pixel on the texture in the uv map gets placed where in the model (which is 3-D). For a quick 2 minute dive checkout this [video](https://www.youtube.com/watch?v=mAcEzlsoad0).

![uv map](images/image_25.jpg)

![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

![](../images/line2.png)

##### `Step 9.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.png)

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

| [previous](../nanites/README.md#user-content-nanites)| [home](../README.md#user-content-ue5-intro-to-static-meshes) | [next](../)|
|---|---|---|
