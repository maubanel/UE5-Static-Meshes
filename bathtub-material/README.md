<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Bathtub Test Material

<sub>[previous](../lightmap/README.md#user-content-lightmap-uvs) • [home](../README.md#user-content-ue4-static-meshes) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Why is the shape so odd in the texture maps, how is this determined? Lets take a closer look at UV Mapping and see how we can test how well a modeler has implemented them.


<br>

---


##### `Step 1.`\|`SUU&G`|:small_blue_diamond:

Create a new Material called `M_Bathtub` and place it in the **Materials** folder. 

![create and apply m_bathtub](images/MBathtubMaterial.jpg)


<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

Apply the **M_Bathtub** material to the static mesh in the **SM_Model** viewer so that it will apply to all future instances.

![assign m_bathtub to sm_bathtub](images/AssignMatToBathtub.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Download [T_Bathtub_M.TGA](../Assets/T_Bathtub_M.TGA) and [T_Bathtub_N.TGA](../Assets/T_Bathtub_N.TGA) and drag them into the **Textures** folder in UE4.

![add two bathtub textures to folder](images/BathtubMaterials.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Open up **T_Bathtrub_N.TGA** and make sure the **Compression Settings** is set to `Normalmap`.
  

![make sure compression is set to normal](images/EnsureNormal.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SUU&G`| :small_orange_diamond:
Open [M_Bathtub.COPY](../Assets/M_Bathtub.COPY) in GitHub and press the <kbd>Raw</kbd> button.  Then select all the text and copy it into your clipboard with <kbd>cntrl C</kbd> (PC) or <kbd>command C<kbd>.

![alt_text](images/CopyPasteMaterial.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond:
The cool thing about materials is that you can cut and paste them between projects.  So Paste it inside the graph of the new **M_Bathtub**.  Make sure the textures are found and that the top texture is the **_M** and the bottom is the texture that ends in **_N**.  

![paste material in unreal](images/PastedMaterial.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:
If you press the <kbd>Apply</kbd> button and render the material you get an error on the main texture sample and needed to change its **Sampler Type** from **Mask** to **Color**.  This was done as the engine misinterpreted the texture's use.

![set texture sample type from mask to color](images/SampleChangeToColor.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

  Connect the bottom **Texture Sample** node to the **Normal** pin.  Press the **Apply button**.  Look at how it adds the illusion of geometry to the sphere.  Pretty cool!

![attach bottom texture to normal map pin](images/AttachNM.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Connect the top pin top **Lerp** pin to **Base Color**.

![connect lerp to base color](images/AttachBaseColor.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`SUU&G`| :large_blue_diamond:

Now in the game engine select **StaticMeshes | SM_Bathtub** then go back to the material and select 

![load bathtub model in material previewer](images/SetPreviewMesh.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: 
 
 Connect the output of the **Multiply** pin to the **Metallic** input on the shader. 
![attach multiply to metallic](images/MultiplyToMetallic.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 
Connect the final empty **Lerp** pin to **Roughness** input pin in the shader.  Press the <kbd>Apply</kbd> button.

![attach lerp to roughness](images/RoughnessApply.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Go back to the game and change the render mode back to **Lit**.

![change back to lit node](images/ReturnToLit.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Add the material **M_Bathtub** to the bathtub model in game if it is not loaded.

![add m_bathtub to game model](images/AddBathtubMaterialToGame.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: 

Now play the game and look at the model and how the material reads in game.

![finished material on bathtub in game](images/AddBathtubMaterialToGame.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

We can also look at how the UV's work by placing a test material in place to see if there are any distortions or obvious issues.  Create a new **Material** called `M_TestTexture` in the **Materials** folder. Drag into the **Textures** folder the [T_UV_Grid.TGA](../Assets/T_UV_Grid.TGA) and see that it has more information than the black and white grid in maya.  It will tell us what part of the texture maps to where. We will use this to see how the UV's project in UE4 instead of Maya this time and you can use this on any model to test the UVs.

![create m_testtexture and add t_uv_grid.TGA](images/AddMaterialTexture.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 17.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Reopen **M_TestTexture** and press the <kbd>T</kbd> key and pressing the **Left Mouse** button.  Load the **Texture** `T_UV_Grid`.

![add a new texture and assign t_uv_grid](images/TUVGrid.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 18.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Attach the **RGB** to **Base Color**. Press the <kb>Apply</kbd> button.  You can see what part of the texture is used on what part of the model.

![attach rgb to base color and apply](images/AttachBaseColor2.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 19.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Duplicate the bathtub in the level and assign the **M_TestTexture**.  Move around the model and look at how the UV's pick portions of the texture map.

![dupe bathtub and assign text texture](images/DupedBathtub.jpg)

https://user-images.githubusercontent.com/5504953/129808512-e0ddc3b0-a473-4ea3-bcca-078bb363426a.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 20.`\|`SUU&G`| :large_blue_diamond: :large_blue_diamond:

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 21.`\|`SUU&G`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

![alt_text](images/.jpg)

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../lightmap/README.md#user-content-lightmap-uvs)| [home](../README.md#user-content-ue4-static-meshes) | [next](../)|
|---|---|---|
