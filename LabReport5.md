Link to my [website](https://github.com/celestewv)

Link to this [page](https://celestewv.github.io/cse15l-lab-reports/LabReport3.html)


*Author:* Celeste Walstrom-Vangor 
<br> *Data Created:* 03/12/23 
<br> *Class:* CSE 15L 


# Blog Post 5:

## “Favorite Lab”

In this lab report, I will be re-exploring my favorite Lab, Lab 3. In that lab report, I found alternate ways to use the command ```find```. 
In this lab report, I am going to explore the ```less``` command.

### Chosen Command: ```less```

### Background Information on the ```less``` Command:

According to the Linux manual page the ```less``` command:
       "Less is a program similar to more(1), but which allows backward
       movement in the file as well as forward movement.  Also, less
       does not have to read the entire input file before starting, so
       with large input files it starts up faster than text editors like
       vi(1).”

*Source: [https://man7.org/linux/man-pages/man1/find.1.html](https://man7.org/linux/man-pages/man1/less.1.html)) found through searching 'find command-line options'*

Regular Use of the ```less``` command:

What I typed: ```less written_1/```

What was produced:

![Image](lessW.png)

### Here Are a Couple Interesting Command-Line Options
Option 1)
```less -F <filename>```

Explanation: This is used when you can remember the name of the file you want to find, but cannot remember where it is saved. It is useful when you want to cd into the correct directory for a certain file, but don’t know where it is located. The 2>/dev/null part of the command is used to silence permission errors, if there are any.

Example 1) 
