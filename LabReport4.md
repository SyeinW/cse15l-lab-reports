# Lab Report 4

## Step 4 (Log into ieng6)
![image](https://user-images.githubusercontent.com/113940184/221774084-7ebe2f3c-8142-4145-9d11-d0b93079d68b.png)

I opened the terminal in VScode using `<ctrl> + <grave>`. Then I logged into the remote server by typing `ssh cs15lwi23aws@ieng6.ucsd.edu` and the pressing `<enter>`. I didn't need to enter in a password since I created a ssh key for my computer. 


## Step 5 (Clone your fork of the repository from your Github account)
![image](https://user-images.githubusercontent.com/113940184/221775444-83cc423d-b7a1-4bbf-8299-838eb81f2a5b.png)

On my github page for the forked repository, I clicked the button labelled "code" and then went into the "ssh" tab. In that tab I copied the ssh link "git@gith...". 

![image](https://user-images.githubusercontent.com/113940184/221774093-e1d36b88-528f-467c-ba8a-95c8acf3dc70.png)

Using the ssh linked I copied earlier, I typed `git clone git@github.com:SyeinW/lab7.git` and pressed `<enter>`. I did this so that I could clone the repository to the remove server I was working on. 


## Step 6 (Run the tests, demonstrating that they fail)
![image](https://user-images.githubusercontent.com/113940184/221774464-d0d0d81b-86ee-459f-8306-4468c22dd20a.png)

After copying the repository I had to cd into it, since I was currently in my home directory. I used the command `cd lab7/` to make lab7 my active directory. 

I copied and pasted the command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` using `<ctrl> + c>`, followed by `<ctrl> + v`, followed by `<enter>`. I got the command from the week 7 lab report section. The command compiles both the tester file and the program file.

I copied and pasted the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore` using `<ctrl> + c>`, followed by `<ctrl> + v`. I got the command from the week 7 lab report section. Then used `<tab> + <tab>` to show all the files in my current directory as I recall the name of the file I needed. Then I typed `L + <tab> + T + <tab>`, followed by `<enter>`. The command runs the tester. 

Just as expected, one of the two tests failed.


## Step 7 (Edit the code file to fix the failing test)
![image](https://user-images.githubusercontent.com/113940184/221776555-67f7796d-8d3d-43a0-abe5-0c8d40312d6d.png)
I typed out the command `nano ListExamples.java` and pressed `<enter>`. This command allows me to edit the code in the ListExamples file within the terminal. 

I used `<ctrl> + w` to move my cursor to the while loop I needed to edit. Once there I had to press `<down> <down>` to get on the correct line, followed by ```<right> <right> <right> <right> <right> <right> <right>``` then I used the `<delete>` key to remove the `1` and replaced it with a `2`. Then I saved the file by using ```<ctrl> + o```, followed by `<enter>`. Finally, I exited nano by using `<ctrl> + x`.
The value that needed changing was 2 down and 7 to the right of the while loop, so I used the arrow keys to access it.


## Step 8 (Run the tests, demonstrating that they now succeed)
![image](https://user-images.githubusercontent.com/113940184/221776664-5273a8cb-d1bf-425a-a254-c3f57497dec1.png)
I ran the command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` again by pressing `<up> <up> <up> <enter>`. The command was 3 up in the search history, so I used up arrow to access it.

Then I ran the command `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTest` again by pressing ```<up> <up> <up> <enter>```. The command was 3 up in the search history, so I used up arrow to access it.

Now instead of there being a failure, both tests passed.


## Step 9 (Commit and push the resulting change to your Github account)
![image](https://user-images.githubusercontent.com/113940184/221777071-74872c3e-465a-4a76-9b8d-e7030c4027ae.png)
