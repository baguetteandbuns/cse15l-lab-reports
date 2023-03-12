# Week 9 Lab Report 5
This lab report goes into more depth about Lab Report 3. I explored the `grep` command in that report, and I will be delving into the `find` command for this week's report.
## Option 1: `-iname` command-line option
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:332$ find ./written_2/ -iname '*GUIDES'
./written_2/travel_guides
```
### Example 2 on File
```
cs15lwi23apw@ieng6-203]:skill-demo1-data:330$ find ./written_2/ -iname '*whattodo.txt'
./written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
./written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
./written_2/travel_guides/berlitz2/Athens-WhatToDo.txt
./written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt                                       
./written_2/travel_guides/berlitz2/Bali-WhatToDo.txt
./written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt
./written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
./written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
./written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt
./written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
./written_2/travel_guides/berlitz2/California-WhatToDo.txt
./written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
./written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt
./written_2/travel_guides/berlitz2/China-WhatToDo.txt
./written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
./written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
./written_2/travel_guides/berlitz2/Crete-WhatToDo.txt
./written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt
./written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt
./written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
./written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
./written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
./written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
```
* Explanation: find file names with the specified pattern but it isn't case sensitive. For instance, when I capitalise "GUIDES" for finding the 'travel_guides' directory wouldn't show up normally. However, since I used `-iname` it does show up. Similarly, for the second example, '-WhatToDo' wouldn't show up using all lowercase letters, but it does due to its case insensitivity.
* Citation: used `man find` on terminal

## Option 2: `-type` command-line option
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:315$ find written_2/ -type d
written_2/
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Castro
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Rybczynski
written_2/travel_guides
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz2
```

### Example 2 on File
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:316$ find written_2/ -type f
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch7.txt
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
written_2/non-fiction/OUP/Fletcher/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch10.txt
written_2/non-fiction/OUP/Fletcher/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch5.txt
written_2/non-fiction/OUP/Fletcher/ch6.txt
written_2/non-fiction/OUP/Fletcher/ch9.txt
written_2/non-fiction/OUP/Kauffman/ch1.txt
written_2/non-fiction/OUP/Kauffman/ch10.txt
written_2/non-fiction/OUP/Kauffman/ch3.txt
written_2/non-fiction/OUP/Kauffman/ch4.txt
written_2/non-fiction/OUP/Kauffman/ch5.txt
written_2/non-fiction/OUP/Kauffman/ch6.txt
written_2/non-fiction/OUP/Kauffman/ch7.txt
written_2/non-fiction/OUP/Kauffman/ch8.txt
written_2/non-fiction/OUP/Kauffman/ch9.txt
written_2/non-fiction/OUP/Rybczynski/ch1.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch3.txt
written_2/travel_guides/berlitz1/HandRHawaii.txt
written_2/travel_guides/berlitz1/HandRHongKong.txt
written_2/travel_guides/berlitz1/HandRIbiza.txt
written_2/travel_guides/berlitz1/HandRIsrael.txt
written_2/travel_guides/berlitz1/HandRIstanbul.txt
written_2/travel_guides/berlitz1/HandRJamaica.txt
written_2/travel_guides/berlitz1/HandRJerusalem.txt
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
written_2/travel_guides/berlitz1/HandRLasVegas.txt
written_2/travel_guides/berlitz1/HandRLisbon.txt
written_2/travel_guides/berlitz1/HandRLosAngeles.txt
written_2/travel_guides/berlitz1/HandRMadeira.txt
written_2/travel_guides/berlitz1/HandRMadrid.txt
written_2/travel_guides/berlitz1/HandRMallorca.txt
written_2/travel_guides/berlitz1/HistoryDublin.txt
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
written_2/travel_guides/berlitz1/HistoryEgypt.txt
written_2/travel_guides/berlitz1/HistoryFWI.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryGreek.txt
written_2/travel_guides/berlitz1/HistoryHawaii.txt
written_2/travel_guides/berlitz1/HistoryHongKong.txt
written_2/travel_guides/berlitz1/HistoryIbiza.txt
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryIsrael.txt
written_2/travel_guides/berlitz1/HistoryIstanbul.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
written_2/travel_guides/berlitz1/HistoryJamaica.txt
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz1/HistoryJerusalem.txt
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
written_2/travel_guides/berlitz1/HistoryLasVegas.txt
written_2/travel_guides/berlitz1/HistoryMadeira.txt
written_2/travel_guides/berlitz1/HistoryMadrid.txt
written_2/travel_guides/berlitz1/HistoryMalaysia.txt
written_2/travel_guides/berlitz1/HistoryMallorca.txt
written_2/travel_guides/berlitz1/IntroDublin.txt
written_2/travel_guides/berlitz1/IntroEdinburgh.txt
written_2/travel_guides/berlitz1/IntroEgypt.txt
written_2/travel_guides/berlitz1/IntroFWI.txt
written_2/travel_guides/berlitz1/IntroFrance.txt
written_2/travel_guides/berlitz1/IntroGreek.txt
written_2/travel_guides/berlitz1/IntroHongKong.txt
written_2/travel_guides/berlitz1/IntroIbiza.txt
written_2/travel_guides/berlitz1/IntroIndia.txt
written_2/travel_guides/berlitz1/IntroIsrael.txt
written_2/travel_guides/berlitz1/IntroIstanbul.txt
written_2/travel_guides/berlitz1/IntroItaly.txt
written_2/travel_guides/berlitz1/IntroJamaica.txt
written_2/travel_guides/berlitz1/IntroJapan.txt
written_2/travel_guides/berlitz1/IntroJerusalem.txt
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt
written_2/travel_guides/berlitz1/IntroLasVegas.txt
written_2/travel_guides/berlitz1/IntroLosAngeles.txt
written_2/travel_guides/berlitz1/IntroMadeira.txt
written_2/travel_guides/berlitz1/IntroMadrid.txt
written_2/travel_guides/berlitz1/IntroMalaysia.txt
written_2/travel_guides/berlitz1/IntroMallorca.txt
written_2/travel_guides/berlitz1/JungleMalaysia.txt
written_2/travel_guides/berlitz1/WhatToDublin.txt
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt
written_2/travel_guides/berlitz1/WhatToEgypt.txt
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz1/WhatToFrance.txt
written_2/travel_guides/berlitz1/WhatToGreek.txt
written_2/travel_guides/berlitz1/WhatToHawaii.txt
written_2/travel_guides/berlitz1/WhatToHongKong.txt
written_2/travel_guides/berlitz1/WhatToIbiza.txt
written_2/travel_guides/berlitz1/WhatToIndia.txt
written_2/travel_guides/berlitz1/WhatToIsrael.txt
written_2/travel_guides/berlitz1/WhatToIstanbul.txt
written_2/travel_guides/berlitz1/WhatToItaly.txt
written_2/travel_guides/berlitz1/WhatToJamaica.txt
written_2/travel_guides/berlitz1/WhatToJapan.txt
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt
written_2/travel_guides/berlitz1/WhatToLasVegas.txt
written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
written_2/travel_guides/berlitz1/WhatToMadeira.txt
written_2/travel_guides/berlitz1/WhatToMalaysia.txt
written_2/travel_guides/berlitz1/WhatToMallorca.txt
written_2/travel_guides/berlitz1/WhereToDublin.txt
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt
written_2/travel_guides/berlitz1/WhereToEgypt.txt
written_2/travel_guides/berlitz1/WhereToFWI.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz1/WhereToGreek.txt
written_2/travel_guides/berlitz1/WhereToHawaii.txt
written_2/travel_guides/berlitz1/WhereToHongKong.txt
written_2/travel_guides/berlitz1/WhereToIbiza.txt
written_2/travel_guides/berlitz1/WhereToIndia.txt
written_2/travel_guides/berlitz1/WhereToIsrael.txt
written_2/travel_guides/berlitz1/WhereToIstanbul.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz1/WhereToJapan.txt
written_2/travel_guides/berlitz1/WhereToJerusalem.txt
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
written_2/travel_guides/berlitz1/WhereToMadeira.txt
written_2/travel_guides/berlitz1/WhereToMadrid.txt
written_2/travel_guides/berlitz1/WhereToMalaysia.txt
written_2/travel_guides/berlitz1/WhereToMallorca.txt
written_2/travel_guides/berlitz2/Algarve-History.txt
written_2/travel_guides/berlitz2/Algarve-Intro.txt
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
written_2/travel_guides/berlitz2/Amsterdam-History.txt
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
written_2/travel_guides/berlitz2/Athens-History.txt
written_2/travel_guides/berlitz2/Athens-Intro.txt
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Bali-History.txt
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
written_2/travel_guides/berlitz2/Barcelona-History.txt
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
written_2/travel_guides/berlitz2/Beijing-History.txt
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/Berlin-History.txt
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
written_2/travel_guides/berlitz2/Bermuda-history.txt
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
written_2/travel_guides/berlitz2/Budapest-History.txt
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt
written_2/travel_guides/berlitz2/California-History.txt
written_2/travel_guides/berlitz2/California-WhatToDo.txt
written_2/travel_guides/berlitz2/California-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-History.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/CanaryIslands-History.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
written_2/travel_guides/berlitz2/Cancun-History.txt
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhatToDo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/Costa-History.txt
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
written_2/travel_guides/berlitz2/CostaBlanca-History.txt
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
written_2/travel_guides/berlitz2/Crete-History.txt
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
written_2/travel_guides/berlitz2/Cuba-History.txt
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt
written_2/travel_guides/berlitz2/Nepal-History.txt
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt
written_2/travel_guides/berlitz2/NewOrleans-History.txt
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
written_2/travel_guides/berlitz2/Poland-History.txt
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-History.txt
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
written_2/travel_guides/berlitz2/PuertoRico-History.txt
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
written_2/travel_guides/berlitz2/Vallarta-History.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
* Explanation: allows to specify the type of file or directory to search for. If you specify `-type f` it only shows file paths. However, `-type d` only shows directory paths. 
* Citation: used command `man find` on terminal

## Option 3: `-size` command-line option
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:361$ find ./written_2 -type d -size -1000M
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2
```
### Example 2 on File
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:358$ find ./written_2 -type f -size -1M
```

* Explanation: this command finds all files in the current directory and its subdirectories that are lesser than 1000 megabytes, and the same thing for files. Since no files are smaller than 1 megabyte, nothing shows up.
* Citation: used command `man find` on terminal

## Option 4: `-delete` command-line option
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:372$ find ./written_2 -name 'OUP' -delete
find: cannot delete './written_2/non-fiction/OUP': Directory not empty
```
### Example 2 on File
```
[cs15lwi23apw@ieng6-203]:skill-demo1-data:362$ find ./written_2 -name '*Cuba*' -delete
[cs15lwi23apw@ieng6-203]:skill-demo1-data:363$ cd ./written_2/travel_guides/berlitz2/
[cs15lwi23apw@ieng6-203]:berlitz2:364$ ls
Algarve-History.txt      Barcelona-History.txt     Canada-History.txt           CstaBlanca-WhereToGo.txt
Algarve-Intro.txt        Barcelona-WhatToDo.txt    Canada-WhereToGo.txt         Nepal-History.txt
Algarve-WhatToDo.txt     Barcelona-WhereToGo.txt   CanaryIslands-History.txt    Nepal-WhatToDo.txt
Algarve-WhereToGo.txt    Beijing-History.txt       CanaryIslands-WhatToDo.txt   Nepal-WhereToGo.txt
Amsterdam-History.txt    Beijing-WhatToDo.txt      CanaryIslands-WhereToGo.txt  NewOrleans-History.txt
Amsterdam-Intro.txt      Beijing-WhereToGo.txt     Cancun-History.txt           Paris-WhatToDo.txt
Amsterdam-WhatToDo.txt   Berlin-History.txt        Cancun-WhatToDo.txt          Paris-WhereToGo.txt
Amsterdam-WhereToGo.txt  Berlin-WhatToDo.txt       Cancun-WhereToGo.txt         Poland-History.txt
Athens-History.txt       Berlin-WhereToGo.txt      China-History.txt            Poland-WhatToDo.txt
Athens-Intro.txt         Bermuda-WhatToDo.txt      China-WhatToDo.txt           Portugal-History.txt
Athens-WhatToDo.txt      Bermuda-WhereToGo.txt     China-WhereToGo.txt          Portugal-WhatToDo.txt
Athens-WhereToGo.txt     Bermuda-history.txt       Costa-History.txt            Portugal-WhereToGo.txt
Bahamas-History.txt      Boston-WhereToGo.txt      Costa-WhatToDo.txt           PuertoRico-History.txt
Bahamas-Intro.txt        Budapest-History.txt      Costa-WhereToGo.txt          PuertoRico-WhatToDo.txt
Bahamas-WhatToDo.txt     Budapest-WhatToDo.txt     CostaBlanca-History.txt      PuertoRico-WhereToGo.txt
Bahamas-WhereToGo.txt    Budapest-WhereoGo.txt     CostaBlanca-WhatToDo.txt     Vallarta-History.txt
Bali-History.txt         California-History.txt    Crete-History.txt            Vallarta-WhatToDo.txt
Bali-WhatToDo.txt        California-WhatToDo.txt   Crete-WhatToDo.txt           Vallarta-WhereToGo.txt
Bali-WhereToGo.txt       California-WhereToGo.txt  Crete-WhereToGo.txt
```

* Explanation: Deletes the files/directories found. However, directories are only deleted if they are empty. For instance, example 1 command tries to find the directory called 'OUP' and delete it. However, since it wasn't empty, it didn't get deleted. On the other hand, I deleted file names with "Cuba" in them, and as you can see no files with "Cuba" in them are there. 
* Citation: used command `man find` on terminal
