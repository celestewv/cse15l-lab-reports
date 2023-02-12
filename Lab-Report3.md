Link to my [website](https://github.com/celestewv)

Link to this [page](https://celestewv.github.io/cse15l-lab-reports/LabReport3.html)


*Author:* Celeste Walstrom-Vangor 
<br> *Data Created:* 01/11/23 
<br> *Class:* CSE 15L 


# Blog Post 3:

## Researching  for Alternate Ways to Use Commands
### Chosen Command: ```find```

### Background Information on the ```find``` Command:

According to the Linux manual page the ```find``` command “searches the directory tree rooted at each given starting-point by evaluating the given expression from left to right, according to the rules of precedence (see section OPERATORS), until the outcome is known (the left hand side is false for and operations, true for or), at which point find moves on to the next file name. If no starting-point is specified, `.' is assumed.”

*Source: [https://man7.org/linux/man-pages/man1/find.1.html](https://man7.org/linux/man-pages/man1/find.1.html) found through searching 'find command-line options'*

Regular Use of the ```find``` command:

```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:507$ find written_2/
written_2/
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch7.txt
written_2/non-fiction/OUP/Castro
written_2/non-fiction/OUP/Castro/chA.txt
written_2/non-fiction/OUP/Castro/chB.txt
written_2/non-fiction/OUP/Castro/chC.txt
written_2/non-fiction/OUP/Castro/chL.txt
written_2/non-fiction/OUP/Castro/chM.txt
written_2/non-fiction/OUP/Castro/chN.txt
written_2/non-fiction/OUP/Castro/chO.txt
written_2/non-fiction/OUP/Castro/chP.txt
written_2/non-fiction/OUP/Castro/chQ.txt
written_2/non-fiction/OUP/Castro/chR.txt
written_2/non-fiction/OUP/Castro/chV.txt
written_2/non-fiction/OUP/Castro/chW.txt
written_2/non-fiction/OUP/Castro/chY.txt
written_2/non-fiction/OUP/Castro/chZ.txt
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Fletcher/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch5.txt
```
*There were more lines of code, but too many to include.

### Here Are 4 Interesting Command-Line Options
Option 1)
```find -name “<name of file?” 2>/dev/null```
Explanation: This is used when you can remember the name of the file you want to find, but cannot remember where it is saved. It is useful when you want to cd into the correct directory for a certain file, but don’t know where it is located. The 2>/dev/null part of the command is used to silence permission errors, if there are any.
Example 1) 
```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:506$ find -name "Bahamas-History.txt" 2>/dev/null
./written_2/travel_guides/berlitz2/Bahamas-History.txt
```
Example 2)
```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:508$ find -name "ch10.txt" 2>/dev/null
./written_2/non-fiction/OUP/Fletcher/ch10.txt
./written_2/non-fiction/OUP/Kauffman/ch10.txt
```

Option 2)
