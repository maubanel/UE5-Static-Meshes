<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Case Study - The Material

<sub>[previous](../case-study/README.md#user-content-case-study---the-model) • [home](../README.md#user-content-ue5-intro-to-static-meshes) • [next](../model-maya/README.md#user-content-setting-up-model-in-maya)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

The materials and textures defines how the model reflects light and is colored.  It defines the pixels, detail in the model and the way it reflects light.  We can combine all the materials on a model in one material/texture sheet or can separate elements. Please note that **Each** material we use increases the render time by a factor of 1.  So the fewer materials we can use on a model the better.

>>> A 3D material is basically what you layer on top of a 3D object, to control the way the object is perceived when rendered. It behaves much the way a material does in the real world - whether that's the way light interacts with its surface, or the nuances of colour, texture, transparency and reflectivity - [The Foundry](https://www.foundry.com/insights/design/3d-materials-explained)

<br>

---


##### `Step 1.`\|`SUU&G`|:small_blue_diamond:



<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

To undertand materials we need to look at how 2-D textures are mapped to the 3-D model. Open up **SM_SoloLSUGlove** and select **UV | UV0** in Unreal.  This is the 3-D shaped unwrapped so that it is like you cut the seams on the glove and laid them out flat (or what the material looked like before it was sewed into a glove.

![uv zero layout of glove](images/UV0GLove.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

So all of our texture maps need to line up with the UV's as it dictates where each pixel will land on the glove. So the color channel assigns a pixel to a location on the UV which then projects it onto the glove like so.  Try to guess where the tiger eye and Nike swoosh will go on the final model in game?

![texture overlayed over geometry](images/image_95.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Import the [T_glove_BC.png](../Assets/T_glove_BC.png), [T_glove_N.png](../Assets/T_glove_N.png) and [T_glove_R.png](../Assets/T_glove_R.png) to the **Textures** folder in the project.
    
![import three glove textures](images/ImportThreeGloveTexture.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SUU&G`| :small_orange_diamond:

Add a new **Material** into the **Materials** folder called `M_Glove`.

![Add m_glove material to game](images/image_97.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond:

Now in that folder please select the **T_glove_BC** texture that decides the color on each area on the model to be applied based on the **UV 0** map.

![select T_glove_BC texture](images/image_98.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Open up **M_Glove** and press the <kbd>T</kbd> key and left click on the graph **or** right click and add a `TextureSample` node to the graph.  It will automatically assign the texture you seleted in the editor which is the glove texture.",

![add texture sample node with base color texture to material](images/image_99.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Drag from the **RGB** pin from the **Texture Sample** node and connect it to the **Base Color**.  Wait a bit and see the sphere update.  Now the texture looks weird as it is applied to sphere without the proper UV's so we can't really see if it works.  Lets fix that by loading the game model we are using.

![base color applied to material](images/image_100.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Go back to the editor and select **StaticMeshes | SM_SoloLSUGlove** in the **Content Browser**.
    
![select glove in editor](images/SelectGlove.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`SUU&G`| :large_blue_diamond:

Open up **M_Glove** and select the far right **Preview** button under the sphere to change it to the mesh you are selecting in the editor.  Press the **Alt** button and turn around to see how the texture now is translated from 2-d back to the 3-d model where the pixels line up correctly. Now do the pixels line up with the UV's?

![load hand model in material](images/image_102.jpg)

![texture overlayed over geometry](images/image_95.jpg)


<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: 

Now go to the **Textures** folder and select **T_Glove_N** for the normal map.  Go back to the **M_Glove** material and add another **TextureSample** node.  It should default with the normal map.

Attach the **RGB** pin to the **Normal** pin in the material.  This adds detail that gives the surface some added geometric detail (it is an illusion) that looks like there are raised and dimpled surfaces on the glove.  This is most pronounced with the air holes. 

![add normal map to glove material](images/AddNormalMap.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Repeat this againm for the **Roughness** texture. Attach the **RGB** pin to the **Roughness** input pin the shader node.  Notice that the glove becomes more reflective as it is a very glossy leather/pleather glove.

![add roughness to material](images/GloveRoughness.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

As usual before we can see this material in game we need to render it by pressing the <kbd>Apply</kbd> button.

![apply change to material](images/ApplyGloveMaterial.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Go into the game and add the material to the glove by adding it to the model in the game window **OR** drag it into the **Materials** slot in the **Details** panel.

![add material to glove in game](images/AddMaterialToGlove.jpg)


<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: 

Now go back to the game, press the <kbd>Build</kbd> button and run the game – look at the glove in the game engine next to our reference model and see if we like how the material was applied and if there are any errors..

![build lighting look at glove in game](images/LitGloveInGame.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

Save progress, submit to source control and upload change to **GitHub** through the **GitHub Desktop** app.

![alt_text](images/SubmitToGithub.jpg)

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - Model in Maya">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../case-study/README.md#user-content-case-study---the-model)| [home](../README.md#user-content-ue5-intro-to-static-meshes) | [next](../model-maya/README.md#user-content-setting-up-model-in-maya)|
|---|---|---|
