![](../images/line3.png)

### Setting Up

<sub>[home](../README.md#user-content-ue4-static-meshes) • [next](../lexicon/README.md#user-content-3-d-lexicon)</sub>

![](../images/line3.png)

We will be working in a third person template and will use the UE4 default and alter it for our needs.  This will give us all we need for a character that we can control."

<br>

---
| `required.software`\|`Static Meshes`| 
| :--- |
| :floppy_disk:You will need to install the latest version of _UE4 4.5.X_ by downloading the [Epic Games Launcher](https://www.epicgames.com/store/en-US/download). You will also need to download [P4V](https://www.perforce.com/downloads/helix-visual-client-p4v)  which is free to sign up for as we will be using version control. I strongly recommned the use of a PC with a good video card to unlock all the powerful features of UE5. On the PC follow these [Windows 10 Turn on Hidden Folders](https://support.microsoft.com/en-us/help/4028316/windows-view-hidden-files-and-folders-in-windows-10) directions. 
|

##### `Step 1.`\|`ITSM`|:small_blue_diamond:

Run the **Epic Games Launcher** and press either **Launch** button to start the editor.

![epic games launcher is open press create new project](images/runEditor.png)

![](../images/line2.png)

##### `Step 2.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: 

Now we will be using **Perforce** for version control.  If you do not have access to a server you can set one up yourself.  Make sure you have access to a server and have a **Depot** to use.  I am using a depot called **UE5 Class** and my **Workspace** is: **maubanel-laptop**.

![select P4 depot](images/p4Depot.png)

![](../images/line2.png)

##### `Step 3.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

You can pick from recent projects or different starting templates with Games, Film/Video & Live Events, Architecture and Automotive Product Designing & Manufacturing as categories.  Lets start by selecting **Games**. Lets select the **Third Person** template.

You can select between C++ and Blueprint.  Since we will not be doing any C++ programming in this exercise we will leave it with its default setting of **Blueprint**.  I am leaving the **Target Platform** at `Desktop` and **Quality Presets** at to `Maximum` as my computer is powerful enough to handle it.  We will leave **Raytracing** off as we will not be using it at the moment and will eventually be depricated from UE5.  We will also not bloat our project size and leave out **Starter Content**.

Choose the folder that holds your **Perforce Workspace | Depot** and call this project `UE4StaticMeshes`.  Press the <kbd>Create</kbd> button to start the create and open the new project.

![select games buton ue4 project installer](images/selectTemplate.png)


![](../images/line2.png)

##### `Step 4.`\|`ITSM`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now we need to hook up source control.  Press **Source Control Off** and connect to source control.  Pick the **Provider** set to `Perforce`.  Click on the **Workspace** drop down to select your local workspace for the machine you are working on.  Press the <kbd>Accept Settings</kbd> button.

![select Perforce source control](images/addSourceControl.png)

![](../images/line2.png)

##### `Step 5.`\|`ITSM`| :small_orange_diamond:

Create a new folder called **Levels**. Now we don't want to use the default level for 3rd person game so press **File | New Level** 
![select Perforce source control](images/newLevel.png)


![](../images/line2.png)

##### `Step 6.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond:


In the editor select the **Edit** menu item then from the drop down menu select **Editor Preferences**. Select **Loading & Saving** tab from the left hand side.  Go to *Source Control* and set **Prompt for Checkout on Asset Modification** to `true` and **Add New Files when Modified** to `true`.  Leave the other two settings at `false` and accept their default editor to deal with merge conflicts. 

https://user-images.githubusercontent.com/5504953/127741784-aa262ff8-e4be-4973-9bb7-4ce7abbc171b.mp4


![](../images/line2.png)

##### `Step 7.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

We will turn this folder into a git repository.  We can do this inside of Unreal.  Click on the **Source Control** button and select **Connect to Source Control**.  This opens up a menu that shows your **Connect to Source Control**.  Then in the menu select **Git (beta version)** as the source control you will be using. Make sure you add a **.gitignore** file, a **README.md** file, a **.gitattributes for Git LFS** file and paste in the GitHub link for the project. Finally **Initialize project with Git** file.

![connect ue4 to github](images/ConnectUe4ToGithub.jpg)

![](../images/line2.png)

##### `Step 8.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Press the **Source Control** button and select `Submit to Source Control`.  Add a comment about the inital commit and press the <kbd>Submit</kbd> button.

![commit to UE4](images/InitialUE4Commit.jpg)

![](../images/line2.png)

##### `Step 9.`\|`ITSM`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now our server has no files on it. We will be using command line (**Terminal** on the mac Or **Git Bash** on the PC). 

In terminal type `git status`.  You will see that it hasn't added files outside of the **Content** folder.  We need to add these seperately. Type 
```
git add .
git commit -m "initial commit"
```

![add and commit new files outside content folder](images/CommitOtherFiles.jpg)

![](../images/line2.png)

##### `Step 10.`\|`ITSM`| :large_blue_diamond:
UE4 still defaults to **Master** branch so we will change it to main.  Type:

```
git branch -M main
git push -u origin main
```
![change branch to main and push](images/ChangeBranchandPush.jpg)

![](../images/line2.png)

##### `Step 11.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: 
Git should return a message saying it has pushed succesfully.  You can also check the github repository to make sure it receive the files.

![succesful git push message](images/ConfirmedPush.jpg)
![github repo showing push](images/.jpg)


![](../images/line2.png)


##### `Step 12.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 

Edit the **README.md** file on GitHub and enter your name as the author and a brief description of the project.  I added `Quick introduction to static meshes (models), preparing them and importing them to Unreal Engine 4`.

![enter name and project description in readme.md file"](images/ReadmeNew.jpg)

![](../images/line2.png)

##### `Step 13.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Now lets add this new repository to **GitHub Desktop** to make it accessible.  Remember **UE4** will just add and commit in engine you have to use another piece of software to push to the server.

Open up **GitHub Desktop** and select **File | Add local repository...**.  Select the location of this project in the root of the `.git` & `.Content` folders. Press the <kbd>Select Folder</kbd> button.

This brings up the **Add local repository** menu.  Press the <kbd>Add repository</kbd> button.  Now fetch from origin to make sure you have the latest from the server.

![Add to GitHub desktop](images/AddToGithubDesktop.jpg)

![](../images/line2.png)

##### `Step 14.`\|`ITSM`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Go to **GitHub** and press the **Add file** button and select **Create new file**. Type in `LICENSE`.  A button pops up on the right and press **Choose a license template**. I recommend the **MIT License**. Add your name and correct the year if necessary. Then you press **Review and submit**. Go back to the main page and select **Compare and pull request**. Press the **Create pull request** button. Select **Merge pull request**, press the **Confirm merge** button and go back to the main page.  The `LICENSE` file should now show up. Now this is on the server so lets bring it onto our laptop.  Go to **GitHub** deskto and press **Fetch Origin** to get the latest. The LICENSE file should now be available locally.

https://user-images.githubusercontent.com/5504953/129390944-574a4285-d77b-410c-b130-3ce19954814a.mp4

![](../images/line2.png)

##### `Step 15.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond: 
Download a thumbnail that you can use on this project [Intro Thumbnail](../Assets/IntroToModels.png). Press the **Settings** button and select **Project Settings**.  Make sure you are in the **Project Description** tab and press the three dots in the **About** tab next to the thumbnail and attach the thumbnail you just downloaded. Enter a project title for the **Description**, **Project Name**.  Put your name as the **Company Name** and you can add your email in **Support Contact**. Add the **Project Displayed Title** and **Project Debug Title Info**.",

![add project thumbnail and names to project settings](images/BasicProjectSettings.jpg)

![](../images/line2.png)

##### `Step 16.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 
Add a new folder to the **Content Browser**, call this folder `Levels`. Go to **File | Save Current** and call the level `TestLevel1` and save it in the **Maps** folder. Go to **Settings | Project Settings** and select the **Maps and Modes** tab.  Change the **Editor Startup Map** and **Editor Default Map** to `Test Level 1`. Close the **Project Settings** window and save again.  

https://user-images.githubusercontent.com/5504953/129446141-d311341b-44fa-4806-acd2-9479f3baa0fc.mp4

![](../images/line2.png)

##### `Step 17.`\|`ITSM`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Press **Source Control | Submit to Source Control** and type in a message of what you just did.  Press **Submit** and you have now succesfully saved the changes locally.

https://user-images.githubusercontent.com/5504953/129446160-222dc30f-1f11-46ca-a750-1e3a49ad4600.mp4


![](../images/line.png)

<!-- <img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - 3-D Lexicon"> -->
![next up next tile](images/banner.png)


![](../images/line.png)

| [previous](../)| [home](../README.md#user-content-ue4-static-meshes) | [next](../lexicon/README.md#user-content-3-d-lexicon)|
|---|---|---|
