# Lab Report 1
## VScode Installation Guide 
The first thing we want to do is install the text editor VScode. Head to [https://code.visualstudio.com/](https://code.visualstudio.com/). Pick the download based on your computer's os. For me, its windows, but for you it might be Linux or OSX. 

![image](https://user-images.githubusercontent.com/113940184/212237079-43bafdc3-9bb2-4d89-81e0-b9ea90851c0d.png)

Once you have installed the VScode setup from their website, open it and complete the setup. 

![image](https://user-images.githubusercontent.com/113940184/212237292-aedbd9d8-3729-4cda-a1cc-0d4b1afef3e8.png)
![image](https://user-images.githubusercontent.com/113940184/212237386-0598dea9-e170-49e6-ae19-46d2db945459.png)
![image](https://user-images.githubusercontent.com/113940184/212237407-ee971a14-561c-484b-bd94-e3030923cedd.png)

After finishing the installation, open up VScode to make sure everything looks right.

![image](https://user-images.githubusercontent.com/113940184/212237769-63413625-50c7-427b-b883-f74d4fcc44e3.png)

I am not using default themes, so yours might look slightly different than mine, but when you first open you should get a "get started" tab. 

## Remote Connection + Git Installation 
**if you are on Linux or OSX you can skip the git installation**

For the Windows users, we want to install git for Windows. To start, we want to head to [https://gitforwindows.org/](https://gitforwindows.org/). 

The page should look similar to this. Click on the Download button to install the setup.
![image](https://user-images.githubusercontent.com/113940184/212239656-e8d27ff8-b6d7-4a6c-a1ca-1bf86f61f8d3.png)

Once you open the setup, you will have to go through a few different setup options. Feel free to choose whatever options you want. I would recommend just using the recommend settings on the setup launcher. 

![image](https://user-images.githubusercontent.com/113940184/212240141-e27245dd-7dce-4a9f-8267-3ab63131b01f.png)

Here is a tutorial on how to use the bash terminal on Windows in VScode [Tutorial](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)

**Start here if you don't need to install git**

We want to open up the terminal in VScode, we can use the keyboard shortcut control/command + \` or we can use the menu option Terminal < New Terminal 

Once we open up the terminal we want to type ```$ ssh cs15lwi23zz@ieng6.ucsd.edu``` into the terminal. "zz" is just an example user in this case, please change the "zz" to your unique user id(also you don't need to type the "$" bash does it for you).

![image](https://user-images.githubusercontent.com/113940184/212244451-6dfe131b-ddc5-443e-950c-b1cec5c7d31f.png)

The terminal should give you something along the lines of "authenticity of host ... can't be established... want to continue connecting." Type yes. You will commonly have to type yes to these, there are a few exceptions where having this come up may be an indication someone is watching what you are doing.

![image](https://user-images.githubusercontent.com/113940184/212244508-bafc58b0-c518-4045-b566-41335266e072.png)

Next we will have to enter in our password. Just like on any other sight, you will not be able to see what you are typing(Do not worry if no characters are showing up that is completely normal) 

![image](https://user-images.githubusercontent.com/113940184/212245114-78f95697-a6ea-4f2e-afd6-3c92a7dc8553.png)

In this image my password is completely typed out but you see nothing. 

![image](https://user-images.githubusercontent.com/113940184/212244885-4397c6b9-a72a-4283-b2e1-3a658749da9b.png)

You should see something similar to this when you log in. It won't be exactly the same as not everyone will connect to the same computer I connected to. 

## Testing the Terminal/Remote Connection
Now that you have done all the work to remotely connect to a computer, you should check out the terminal. Try using some different commands to get around the directory. You can go almost anywhere(except where you don't have permissions to be). 

*commands to try*
* cd ~
* cd 
* cd ..
* ls - lat
* ls -a
* ls <directory>

**In order to log out of the remote server use:** Control+D or type "exit" in the terminal
**Bonus** - You can open more than one terminal in VSCode by clicking on the plus icon 
  
![image](https://user-images.githubusercontent.com/113940184/212246604-35cc4787-bb1f-441c-9386-527eaa9e117b.png)
