Installation guide (JDK)
---

**Step 1:**
---
 Open the <https://www.oracle.com/java/technologies/javase-downloads.html>  url in the browser and it will navigate to the official Oracle Java downloads page.

**Step 2:** 
---
- Select the version of Java which we want to download.
- Select the operating system.
- Scroll down to the page and click on the URL option suitable for your computer Operating system. But for a 64-bit machine, choose the software name ending with x64.  
![jdk1](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/04499dfd-d7ca-4083-a787-4d13120f5037)


**Step 3:** 
---
![Aspose Words f34fb923-a537-4b9b-8671-08be93095383 006](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/319eca46-36cc-403a-9f4a-5946be06f923)

After the downloading procedure is complete, we need to run the installer



**Step 4:** 
---
Once Java installation wizard opens, click on the Next button as shown below:

![Aspose Words f34fb923-a537-4b9b-8671-08be93095383 007](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/c5f5eb93-8e2a-4186-988a-8007dafc8afe)













**Step 5:** 
---
Again click on the Next button if we wish to install Java development kit in the default directory(encircled with green color), or we can change this directory by clicking on Change button.  

![Aspose Words f34fb923-a537-4b9b-8671-08be93095383 008](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/52a0cd37-eb3b-4363-9f37-5dc9df74fe86)











**Step 6:** 
---
The installation will begin as shown below:

![Aspose Words f34fb923-a537-4b9b-8671-08be93095383 009](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/4ce206bd-774b-4903-964d-3f159b5668ca)






**Step 7:**
---
Finally, we can click on the Close button after the confirmation window appears which says that the Java is installed.

![Aspose Words f34fb923-a537-4b9b-8671-08be93095383 010](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/9909b659-b2a7-4171-94cc-75bcdd463cc0)












**Setting up Environment in Java**
---
- After downloading,  Once you install Java on your device, you have to set up the environment variable.

**Step 1**:
---
Locate the JDK Installation Folder:

After installing the JDK, it's important to find out where it's installed. By default, java is installed in the “C:\Program Files\Java\jdk\bin” folder OR “C:\Program Files(x86)\Java\jdk\bin”. In case, you have installed Java at any other location, then add that path.

**C-drive  à Program Filesàjava àjdk à bin (copy the path)**

**Step 2:**
---
Go to the search bar and search **f**or **Environment variable ->** click on **Edit system Environment variable.**

Under the Advanced System Setting option click on **Environment Variables** as highlighted below**.**

![env 2](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/f9451cdc-064c-4d50-8da4-9161a5d00c98)











**Step 3**
---
Now, you have to alter the “**Path”** variable under System variables so that it also contains the path to the Java environment. Select the “Path” variable and click on the **Edit button** as highlighted below.

![env-2](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/8e0fffc8-f219-47fa-9500-dddac7527257)





**Step 4:**
---
You will see a list of different paths, Click on the **New** button, and then add the path where Java is installed. By default, java is installed in the “C:\Program Files\Java\jdk\bin” folder OR “C:\Program Files(x86)\Java\jdk\bin”. In case, you have installed Java at any other location, then add that path.









![env-3](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/9c59425b-9c3d-42bd-b85e-833d6fad77cf)












**Step 5**: 

Click on OK, Save the settings, and you are done !! Now to check whether the installation is done correctly, open the **command prompt** and type **java --version**. You will see that java is running on your machine.

[ref1]: Aspose.Words.f34fb923-a537-4b9b-8671-08be93095383.002.png
