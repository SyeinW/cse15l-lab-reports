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


Once we open up the terminal we want to type 

```$ ssh cs15lwi23xx@ieng6.ucsd.edu```

into the terminal. "xx" is just an example user in this case, please change the "xx" to your unique user id(also you don't need to type the "$" bash does it for you).



The terminal should give you something along the lines of "authenticity of host ... can't be established... want to continue connecting"(Because you haven't logged into the server before). 

![image](https://user-images.githubusercontent.com/113940184/212244508-bafc58b0-c518-4045-b566-41335266e072.png)

Type yes. You will commonly have to type yes to these, there are a few exceptions where having this come up may be an indication someone is watching what you are doing.

Next we will have to enter in our password. Just like on any other site, you will not be able to see what you are typing(Do not worry if no characters are showing up that is completely normal). 

```
$ ssh cs15lwi23xx@ieng6.ucsd.edu
The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.238)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Password: 
```

Or if you make the same mistake I did and took too long to enter in your password the terminal will kick you out. Its no big deal you just have to reenter the ssh command. Should look similar to this

![image](https://user-images.githubusercontent.com/113940184/212245114-78f95697-a6ea-4f2e-afd6-3c92a7dc8553.png)

**In the image above, my password is completely typed out but you see nothing.**


We are now logged into the terminal so everything you see below is happening on the remote server, not on your computer. 

![image](https://user-images.githubusercontent.com/113940184/212244885-4397c6b9-a72a-4283-b2e1-3a658749da9b.png)

You should see something similar to this when you log in. It won't be exactly the same as not everyone will connect to the same computer I connected to. 

## Testing the Terminal/Remote Connection
Now that you have done all the work to remotely connect to a computer, you should check out the terminal. Try using some different commands to get around the directory. You can go almost anywhere(except where you don't have permissions to be). 

*commands to try*
* cd ~
* cd 
* cd ..
* ls -lat
* ls -a
* cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lwi23/public/hello.txt

Feel free to run these commands in any order or even try some other commands you may know. 

Your data will be safe on the server assuming you only save it to your personal directory. No other student can access your personal home directory located within the server. For instance if I did ```cd /home/linux/ieng6/cs15lwi23/apn``` I would get a message back ```-bash: cd: cs15lwi23apn: Permission denied``` because that it not my home directory.

The ```cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/``` was the most interesting command for me. I did not know what it did prior to running it. Basically it copied the hello.txt file in path /home/linux/ieng6/cs15lwi23/public/hello.txt to my home directory. It was also interesting in that I had to research a little on the differences between scp and cp. For the most part, you use scp when sending data to a server `ssh ...` so that your data will be encrypted while it travels from computer to server. And you use cp when copying files from one path on your computer to another



**In order to log out of the remote server use:** Control+D or type "exit" in the terminal

You can open more than one terminal in VSCode by clicking on the plus icon 
  
![image](https://user-images.githubusercontent.com/113940184/212246604-35cc4787-bb1f-441c-9386-527eaa9e117b.png)

