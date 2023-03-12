Link to my [website](https://github.com/celestewv)

Link to this [page](https://celestewv.github.io/cse15l-lab-reports/LabReport3.html)


*Author:* Celeste Walstrom-Vangor 
<br> *Data Created:* 02/11/23 
<br> *Class:* CSE 15L 


# Blog Post 3:

## Researching  for Alternate Ways to Use Commands
### Chosen Command: ```find```

### Background Information on the ```find``` Command:

According to the Linux manual page the ```find``` command:
       "Less is a program similar to more(1), but which allows backward
       movement in the file as well as forward movement.  Also, less
       does not have to read the entire input file before starting, so
       with large input files it starts up faster than text editors like
       vi(1).”

*Source: [https://man7.org/linux/man-pages/man1/find.1.html](https://man7.org/linux/man-pages/man1/less.1.html)) found through searching 'find command-line options'*

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
```find ~/<directory>/ -name "*txt" -exec grep -Hi <word to look for> {} \;```

Explanation: This is useful to help you search files for a specific content that you are looking for. Maybe a word or phrase, this can help you find which file it is in.

Example 1)
```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:530$ find written_2/ -name "*txt" -exec grep -Hi Lucayans {} \;
written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
Example 2)
```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:533$ find written_2/ -name "*txt" -exec grep -Hi giraffe {} \;
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt: giraffes. There are also beautiful big cats and a large “Plains of
written_2/travel_guides/berlitz1/WhereToIndia.txt: giraffe, which indicates the Indian west coast’s early contact with
written_2/travel_guides/berlitz1/WhereToItaly.txt: burly fellows blowing molten globules into cute little green giraffes.
written_2/travel_guides/berlitz1/WhereToMadeira.txt: which at over 5 m (171/2 ft) tall, stands almost as high as a giraffe.
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:Zoological figurines. Turtles, elephants, giraffes, and, most prevalent, images of Puerto Rico’s beloved tree frog, the coquí.

```

Option 3)
```find ~ -type <type of file>```

Explanation: Useful if you are looking for all of a certain type of file within a large directory and all of its subdirectories.

Example 1)
```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:535$ find ~ -type f
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.bash_profile
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.bashrc
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.cshrc
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.kshrc
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.locallogin
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.login
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.procmailrc
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.profile
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.zprofile
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.zshenv
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.zshrc
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.cache/abrt/lastnotification
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.modulesbegenv
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.motd
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.bash_history
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/wavelet/.git/info/exclude
```
*There were more lines of results, but too many to include.

Example 2)
```
[cs15lwi23aky@ieng6-202]:skill-demo1-data:540$ find ~ -type f -empty
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/.motd

```

Option 4)
```find <path> -mtime -<number of day>```

Explanation: Useful command to help locate all files that have not been modified in the specified amount of time.


Example 1)
```
[cs15lwi23aky@ieng6-201]:written_2:516$ find /home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2 -mtime -7
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch1.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch14.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch15.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch2.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch3.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch6.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch7.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch8.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch9.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Berk
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Berk/CH4.txt
```

*There were more lines of code, but too many to include.

Example 2)
```
[cs15lwi23aky@ieng6-201]:written_2:519$ find /home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2 -mtime -365
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch1.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch14.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch15.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch2.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch3.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch6.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch7.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch8.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Abernathy/ch9.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Berk
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Berk/CH4.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Berk/ch1.txt
/home/linux/ieng6/cs15lwi23/cs15lwi23aky/skill-demo1-data/written_2/non-fiction/OUP/Berk/ch2.txt
```
*There were more lines of code, but too many to include.


*Every example was found from this source: [https://www.redhat.com/sysadmin/linux-find-command](https://www.redhat.com/sysadmin/linux-find-command) found through searching 'cool ways to use the find command-line tool'*
