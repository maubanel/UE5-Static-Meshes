![](../images/line3.png)

### Setting Up II

<sub>[previous](../setting-up/README.md#user-content-setting-up) • [home](../README.md#user-content-ue5-intro-to-static-meshes) • [next](../lexicon/README.md#user-content-3-d-lexicon)</sub>

![](../images/line3.png)

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Finish setting up our level.

<br>

---


##### `Step 1.`\|`ITSM`|:small_blue_diamond:

If Unreal is closed reopen the **UE5StaticMesh** project.  Select the **Landscape** asset in the **Outliner** of the **Experimental** level. Add **Material** `MI_Landscape` to the **Landscape Material** slot. 

![add MI_Landscape material to landscape](images/matLandscape.png)

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

Now it will be like we are really high in the atmosphere based on the height of our previous landscape that this was built on. So the numbers for where surfaces appear and disappear are wrong.

![terrain looks wrong](images/looksWrong.png)

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

On the landscape change the **Transform | Location | Z** to `-20000` (-20,000). Now we are in a rocky world.  That will do.

![lower z on landscape](images/MinusTwenty.png)

![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

We do not need the **Third Person | Maps** folder anymore so you can delete it. Right click the **Maps** folder then select the <kbd>Delete</kbd> option.

![delete maps folder](images/deletethirdp.png)

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Right click on hte the **Content** folder and select **Fix Up Redirectors in Folder**.

![fix up redirects in all folders](images/fixRedirects.png)

![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:

 Make sure your `.p4ignore` is at the root of your workspace. You should have two project folders if you completed the **HelloWorld** walk through.

![add .p4ignore file to project](images/p4ignore.png)

![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:


Select the **File | Save All** then press the <kbd>Source Control</kbd> button and select **Submit Content**.  If you are prompted, select **Check Out** for all items that are not checked out of source control. Update the **Changelist Description** message and with the latest changes. Make sure all the files are correct and press the <kbd>Submit</kbd> button. A confirmation will pop up on the bottom right with a message about a changelist was submitted with a commit number.

![save all and submit to perforce](images/submitP4.png)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:




![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE"> -->
![next up next tile](images/banner.png)

![](../images/line.png)

| [previous](../setting-up/README.md#user-content-setting-up)| [home](../README.md#user-content-ue5-intro-to-static-meshes) | [next](../lexicon/README.md#user-content-3-d-lexicon)|
|---|---|---|
