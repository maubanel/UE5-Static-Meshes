<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Edge Normals in Practice

<sub>[previous](../lexicon/README.md#user-content-3-d-lexicon) • [home](../README.md#user-content-ue4-static-meshes) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Lets look at how edge normals can change the look of an edge on a shape.  Lets also look at importing static meshes into Unreal. 
<br>

---


##### `Step 1.`\|`SUU&G`|:small_blue_diamond:

The file format most used is a `.fbx` file. **[FBX](https://en.wikipedia.org/wiki/FBX)**
![alt_text](images/.jpg).  This is a 3-D format that can describe all the parts of a 3-D model and is supported by a large variety of 3-D software packages.  Interoperability between 3-D packages was the key motivation behind the format.

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

Download [SM_Hard_Edge.FBX](../Assets/SM_Hard_Edge.FBX) and [SM_Soft_Edge.FBX](../Assets/SM_Soft_Edge.FBX).  

![download SM_Hard_Edge.FBX and SM_Soft_Edge.FBX](images/DownloadCubes.jpg)


<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Right click in the **Content Browser** tab and add a folder called `StaticMeshes`.  Make sure it is root to **Content**.  

![added StaticMeshes folder](images/AddStaticMeshesFolder.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SUU&G`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

One way to import static meshes that are `.fbx` files is to drag and drop them tinot the folder. Drag the two models by shift selecting them and dragging them into the **Content Browser**.  

![drag and drop SM_Hard_Edge.FBX and SM_Soft_Edge.FBX into Static Meshes folder](images/DragAndDropImport.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SUU&G`| :small_orange_diamond:

Now this brings up the **FBX Import Options** menu.  Lets look at the important options we will use ythe most.  First there are only two types of models, **Static Meshes** and **Skeletal Meshes**.  So the first option if **Skeletal Mesh** is deselected it treats the fbx as a **static mesh**.

We tick **Generate Missing Collisions** as I didn't provide collisions for this model when I created it in **Maya**.  I also didn't create **Lightmap UV's** so we will click that tho `true`.  We also need to set **Transform Vertex to Absolute** to avoid issues when importing collisions with your mesh. We also do not want to create new materials for this model.  Typically we do our materials in a third party package or directly in **Unreal** so typically this is set to **Do Not Create Material** with **Import Textures** set to `false`. Press the <kbd>Import All</kbd> button and import both models into the **StaticMeshes** folder.

![staic mesh settings](images/StaticMeshImportSettings.jpg)
<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond:

Open up both models in the **UE4** and press the <kbd>Normals</kbd> previewer.  You will see that the model with the soft (rounded) edge has one green edge normal and the sharp edge has three edge normals.

![soft and hard edge normals](images/LookAtEdgeNormals.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

We can also look at the vertex locations on the model by selecting <kbd>Verteces</kbd>

![vertex locations on model](images/VertextLocation.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Lets look at the faces of the model and not render the material and texture.  We first shoudl turn off the **Show Floor** and **Show Environment** in the **Preview Scene Settings** tab.

![turn off floor and environment in preview window](images/TurnOffBackground.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`SUU&G`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

We can now view the cube as a wireframe by pressing the <kbd>Wireframe</kbd> button.  Now even though I modeled using **Quads** in **Maya** it converted them into triangles when importing.  You can see that I have **10 faces** that comprises of **20 triangles**.  We care about how many triangles there are as this affects our performance.

![view cube in wireframe](images/WireframeModelViewer.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`SUU&G`| :large_blue_diamond:

Run the game and position the two cubes in the level.  Move around and look at the edge. One is definitely soft and the other is sharp.  This is not created by the polygons but by the edge normals.

https://user-images.githubusercontent.com/5504953/129449924-235a4913-91a6-4381-9b9c-72026498472b.mp4

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: 

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`SUU&G`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: 

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 17.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 18.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 19.`\|`SUU&G`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 20.`\|`SUU&G`| :large_blue_diamond: :large_blue_diamond:

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 21.`\|`SUU&G`| :large_blue_diamond: :large_blue_diamond: :small_blue_diamond:

![alt_text](images/.jpg)

___

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT TITLE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../lexicon/README.md#user-content-3-d-lexicon)| [home](../README.md#user-content-ue4-static-meshes) | [next](../)|
|---|---|---|
