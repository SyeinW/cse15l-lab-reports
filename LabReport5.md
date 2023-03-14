# Lab Report 5

I chose to write a bash script to quickly do the week 7 lab speed contest.

My best time was about 1 minute during the Lab contest, but using a bash script you can do it in less than 5 seconds.

For my implementation, I used two different bash scripts.

## Bash Script 1 

![image](https://user-images.githubusercontent.com/113940184/224901809-86a36455-e9bf-492d-9704-06a69e472199.png)

The first line uses the `read` command to get a user input for the variable `user_name`. In my case, the `user_name` variable will be assigned to `cs15lwi23aws@ieng6.ucsd.edu`.

The second line connects into the remote server using the `user_name` you entered and it also runs the command `bash Lab7Bash`. `Lab7Bash` is our second bash script.

## Bash Script 2 

![image](https://user-images.githubusercontent.com/113940184/224903962-42ee6332-c3b8-43e6-aa69-f76c188da95f.png)

This bash Script just follows lab steps in order. 

The hardest part with this Bash script was figuring out how to edit ListExamples.java. I tinkered with using nano, but realized that I have no idea how to get a bash script to use nano/know if it is possible. I tried looking for resources online but didn't find anything, even tried chatgpt.

![image](https://user-images.githubusercontent.com/113940184/224904989-7ec145e5-48ae-42fd-8ac2-2f32147ee8c8.png)

![image](https://user-images.githubusercontent.com/113940184/224905020-1132b6d6-f6f0-43a7-a7d9-d038d17b0db0.png)

Maybe I messed something up, but on my end using `nano ListExamples.java` only resulted in `Error opening terminal:unknown`

My solution to editing the ListExamples.java was having a fixed file that would overright the bad file using `cat` and `>`

I also added the `rm` command at the end to speed up the process of restarting the speedrun. I don't think there is a way to use a bash script to delete a fork/fork a repository so I think that is out of the question. 
