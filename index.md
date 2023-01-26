
Link to my [website](https://celestewv.github.io/cse15l-lab-reports)


*Author:* Celeste Walstrom-Vangor 
*Data Created:* 01/11/23 
*Class:* CSE 15L 




# Blog Post 1:
## How to log into a course-specific account on ieng6

Welcome to CSE 15L! This tutorial is going to show you how to install an account specific to the CSE 15L course account on ieng6, but could be generalized for other courses. 
____________________________________________________________________________________________________

## Installing VScode:

The first step is going to be installing Visual Studio Code (VSC). Follow the link https://code.visualstudio.com/, and follow the instructions to download and install it on your computer. The directions may be different for Mac vs. Window users, but once it’s installed you should have the app. Once you have installed the app, it should show up in your applications folder and you can move it to your dock (as shown in the screenshot below), if you prefer.

Once it is successfully downloaded, open the app. It should look similarly to the screenshot shown before. It may not have the folders on the side as the screenshot does, or be in a different color, but either will work.

<!--dock image-->
<img width="1404" alt="Screen Shot 2023-01-11 at 11 59 50 AM" src="https://user-images.githubusercontent.com/122484285/211909958-3c643b3e-ba82-4e50-9636-08de6228bd02.png">
Here is an example of a dock with VScode in it. Fifth from the left-end is the app.

<!--vscode image-->
<img width="1440" alt="Screen Shot 2023-01-11 at 11 20 55 AM" src="https://user-images.githubusercontent.com/122484285/211910243-02cd6916-23f8-41e9-97ed-4029da5ecdd4.png">
To make sure you got the right version/correct app, here is what the app should look like if you open it (or something similar). If you're getting an error message reach out to one of your classmates, tutors, or TAs for assistance. 
______________________________________________________________________________________________________

## Remotely Connecting:

Now we want to create an account/connect to our account so we can access the CSE 15L computer system from anywhere! This is a skill that will come in hand for many jobs or other institutions. So cool right?

The first step will be going to this link https://sdacs.ucsd.edu/~icc/index.php and finding out what your 2-4 letter unique code is. For example, it should look something like this: cs15lwi23xxx. If you know your password, you’re good to go, otherwise create a new one!

Now let's open up our computer terminal and type in the following information:
```
ssh cs15lwi23aky@ieng6.ucsd.edu
```
<replay 'aky' with whatever your individual letters are>

<img width="565" alt="Screen Shot 2023-01-11 at 12 06 08 PM" src="https://user-images.githubusercontent.com/122484285/211909954-37ed5dbb-fcb4-4b3b-909a-5f0c2ca59888.png">

Replace the ‘aky’ with whatever letters follow your ‘cs15lwi23’.
Next, enter your password. Don’t worry, it’s not supposed to show up as you type!

Now you should get the following message:
```
The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established. RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec. Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Password:
```
Put yes. Then:


<img width="564" alt="Screen Shot 2023-01-11 at 12 11 16 PM" src="https://user-images.githubusercontent.com/122484285/211909953-28eed27d-59cd-49e1-b4a0-20c35034c041.png">

<img width="567" alt="Screen Shot 2023-01-11 at 12 11 28 PM" src="https://user-images.githubusercontent.com/122484285/211910782-d7625c2f-f1a7-4d06-8046-9c59515b357f.png">

Congratulations! Now your portable computer is connected to an individual computer in the CSE Basement. From now on your computer will be refered to as the _client_ and the basement computer as the _server_.
______________________________________________________________________________________________________

## Trying Some Commands:

Now that we’re in, let’s try some awesome commands!

Some important commands could be:
Here are some specific useful commands to try:
```
cd ~
cd
ls -lat
ls -a
```
`ls <directory>` where <directory> is /home/linux/ieng6/cs15lwi23/cs15lwi23abc, where the abc is one of the other group members’ username
```cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/```
```cat /home/linux/ieng6/cs15lwi23/public/hello.txt```


Here’s what one example should look like:

<img width="555" alt="Screen Shot 2023-01-11 at 12 17 59 PM" src="https://user-images.githubusercontent.com/122484285/211909945-1bbafc4f-eb30-4bca-b664-c87f77b75cd4.png">



Then you should be all done! Happy coding!









