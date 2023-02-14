# Lab Report 3 - Week 6
I have chosen the `grep` command for this assignment
## Option 1: `-i` command-line option: `--ignore-case`
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-201]:written_2:171$ grep -ir "soledad" 
travel_guides/berlitz2/Cuba-WhereToGo.txt:The Jardín Botánico Soledad, 18 km (11 miles) outside Cienfuegos on the road to Trinidad, is the oldest botanical garden in Cuba (it dates to 1899) and one of the finest tropical gardens in the world. Ask at the tourist office in Cienfuegos about guided tours of the gardens.
travel_guides/berlitz2/Vallarta-WhereToGo.txt:The centerpiece of downtown is its zócalo (central plaza), heavily laden with shade trees and bordered by Acapulco’s principal church, Nuestra Señora de la Soledad, as well as numerous, inexpensive cafés and restaurants. This church is one of the more notable structures in Acapulco The blue onion-like domes are more Russian Orthodox than Roman Catholic in style — in fact, the structure was originally built as a movie set. Every Sunday evening, local bands serenade the plaza’s numerous visitors. Across from the plaza is the beach, Playa Manzanillo, where sport-fishing charters, as well as pleasure and excursion boats depart.
```
### Example 2 on File
```
[cs15lwi23apw@ieng6-201]:written_2:173$ grep -i "borda" ./travel_guides/berlitz2/Vallarta-WhereToGo.txt
Among the numerous silversmith shops here, you’ll find several landmarks. Most notable is the Church of San Sebastián and Santa Prisca, located on Plaza Borda. This elaborate church was built by silver magnate Joseph Borda as a show of his appreciation to the town and to the Almighty for the wealth he accumulated here. Additional attractions are the Museo de Taxco Guillermo Spratling, featuring a collection of pre-Columbian artifacts, the Silver Museum, and the Casa Humboldt, which details the past of this historic town.
```
* Explanation: allows the search to be case insensitive. For instance, even though the file contains "soledad" with a capital S, our argument didn't contain the capital s. Since the command `-i` allowed case insensitive searching, we were still able to locate the word in the file. It is useful as now we can search for a specific word through an entire directory. For instance, I don't remember the file name but I remember a specific word in the document.
* Citation: used command `man grep` on terminal
## Option 2: `-w` command-line option: `--word-regexp`
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-201]:written_2:179$ grep -wr "Burger" ./
./travel_guides/berlitz2/Vallarta-WhereToGo.txt:The best known image of Puerto Vallarta is the Iglesia de Guadalupe (Guadalupe Church), dedicated to the Virgin of Guadalupe, and topped by a copy of the crown worn by Empress Carlota in the 1860s. Wife of Emperor Maximillian, the only emperor of Mexico to be appointed by a foreign power, she is considered to be a tragic heroine. Golden angels hold up the bell tower, and the interior is decorated with a few muted murals. The church overlooks Puerto Vallarta’s plaza with its central bandstand and adjacent Palacio Municipal (City Hall). This plaza is representative of plazas throughout Mexico; what reminds you that you are in an international tourist town are the surrounding signs for Burger King, Subway, and Hooters.
```
### Example 2 on File
```
[cs15lwi23apw@ieng6-201]:written_2:180$ grep -w "marks" ./travel_guides/berlitz2/Vallarta-WhereToGo.txt
Playa Marinero extends from the central beach to the rocky outcropping, Rocas del Morro, that marks the beginning of Zicatela and its impressive waves. Along Marinero, several rustic restaurants offer beach chairs and a place to pass the day while enjoying cool drinks and fresh seafood.
```
* Explanation: allows matching only complete words that match the pattern specified. For instance, in the second example, if they file contained the word "landmarks" it would still show up on the searches found normally. Since we used the command `-w` a search is only matched if the pattern is an independent word. It is a useful command, as it will help us eliminate irrelevant searches, especially when there are a lot of matches.
* Citation: used command `man grep` on terminal

## Option 3: `n`, `--line-number`
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-201]:written_2:201$ grep -nr "gardens and p" ./travel_guides 
./travel_guides/berlitz1/HandRHawaii.txt:174:        lanais face the beach and an atrium complex of gardens and pools in
./travel_guides/berlitz2/California-WhereToGo.txt:87:A combination of engineering genius and shady business deals brought water hundreds of miles across mountains and desert to slake the city’s thirst and nurture its lush gardens and palm trees. An abundance of space then allowed the city to sprawl, but distance was no problem — cheap oil and the car produced a vast freeway system, which links the coast, the hills, and the farthest-flung valleys in one huge metropolitan region. Visitors flying into L.A. at night get a grand view of the network of traffic arteries, with cars and trucks surging along like blood corpuscles pumping through the veins of some living organism.
./travel_guides/berlitz2/Paris-WhereToGo.txt:61:East of the Palais-Royal, Les Halles was for centuries the site of the capital’s central food markets (now in a more spacious, if less colorful, location at Rungis, near Orly). To widespread regret, Victor Baltard’s great cast-iron and glass pavilions were torn down in the 1970s. Eventually, gardens, children’s playgrounds, and the maze-like, partly below-ground shopping mall, Forum des Halles, transformed the site. Saturdays bring throngs of teenagers from the suburbs to shop, watch films, roller skate, munch fast food, and just hang out. The liveliest meeting place is around the monumental Renaissance Fontaine des Innocents (once part of a cemetery). Bars, restaurants, and late-night brasseries line the adjoining rue Berger and the streets leading off it. Clubs and discos come alive at midnight and stay open to dawn, especially on weekends. Away from the gardens and playgrounds, the quarter has its seedy side: drink and drugs, pickpockets and prostitutes. Rue St-Denis, once primarily a red-light district, is now pedestrianized, but still has its share of sex shops.
```
### Example 2 on File
```
[cs15lwi23apw@ieng6-201]:written_2:198$ grep -n "garden" ./travel_guides/berlitz1/IntroJapan.txt 
65:        moss-covered temple garden or in the alcove of a traditional restaurant
219:        Zen temple rock garden is shattered by recorded announcements blaring
223:        grocery store; and when parks, gardens, and hallowed temples are ringed
260:        beauties of kabuki theater, Zen rock gardens, and ikebana flower
```
* Explanation: precede each line of output with its line number in the file. For instance, in the second example the output also includes the line numbers the word "garden" can be found in the file. It is a useful command for locating the position of the word we want to find in the file, as normally we can only see the word in excerpt terminal shows us. We should use this command for finding the exact location.
* Citation: used command `man grep` on terminal

## Option 4: `-c`, `--count`
### Example 1 on Directory
```
[cs15lwi23apw@ieng6-201]:written_2:207$ grep -cr "garden" ./travel_guides/berlitz2/
./travel_guides/berlitz2/Algarve-History.txt:0
./travel_guides/berlitz2/Algarve-Intro.txt:0
./travel_guides/berlitz2/Algarve-WhatToDo.txt:0
./travel_guides/berlitz2/Algarve-WhereToGo.txt:7
./travel_guides/berlitz2/Amsterdam-History.txt:0
./travel_guides/berlitz2/Amsterdam-Intro.txt:0
./travel_guides/berlitz2/Amsterdam-WhatToDo.txt:0
./travel_guides/berlitz2/Amsterdam-WhereToGo.txt:3
./travel_guides/berlitz2/Athens-History.txt:0
./travel_guides/berlitz2/Athens-Intro.txt:0
./travel_guides/berlitz2/Athens-WhatToDo.txt:2
./travel_guides/berlitz2/Athens-WhereToGo.txt:5
./travel_guides/berlitz2/Bahamas-History.txt:1
./travel_guides/berlitz2/Bahamas-Intro.txt:0
./travel_guides/berlitz2/Bahamas-WhatToDo.txt:0
./travel_guides/berlitz2/Bahamas-WhereToGo.txt:3
./travel_guides/berlitz2/Bali-History.txt:0
./travel_guides/berlitz2/Bali-WhatToDo.txt:0
./travel_guides/berlitz2/Bali-WhereToGo.txt:10
./travel_guides/berlitz2/Barcelona-History.txt:0
./travel_guides/berlitz2/Barcelona-WhatToDo.txt:0
./travel_guides/berlitz2/Barcelona-WhereToGo.txt:1
./travel_guides/berlitz2/Beijing-History.txt:1
./travel_guides/berlitz2/Beijing-WhatToDo.txt:0
./travel_guides/berlitz2/Beijing-WhereToGo.txt:17
./travel_guides/berlitz2/Berlin-History.txt:0
./travel_guides/berlitz2/Berlin-WhatToDo.txt:0
./travel_guides/berlitz2/Berlin-WhereToGo.txt:5
./travel_guides/berlitz2/Bermuda-WhatToDo.txt:0
./travel_guides/berlitz2/Bermuda-WhereToGo.txt:8
./travel_guides/berlitz2/Bermuda-history.txt:0
./travel_guides/berlitz2/Boston-WhereToGo.txt:6
./travel_guides/berlitz2/Budapest-History.txt:0
./travel_guides/berlitz2/Budapest-WhatToDo.txt:0
./travel_guides/berlitz2/Budapest-WhereoGo.txt:7
./travel_guides/berlitz2/California-History.txt:0
./travel_guides/berlitz2/California-WhatToDo.txt:0
./travel_guides/berlitz2/California-WhereToGo.txt:11
./travel_guides/berlitz2/Canada-History.txt:0
./travel_guides/berlitz2/Canada-WhereToGo.txt:23
./travel_guides/berlitz2/CanaryIslands-History.txt:0
./travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:0
./travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:6
./travel_guides/berlitz2/Cancun-History.txt:0
./travel_guides/berlitz2/Cancun-WhatToDo.txt:1
./travel_guides/berlitz2/Cancun-WhereToGo.txt:3
./travel_guides/berlitz2/China-History.txt:0
./travel_guides/berlitz2/China-WhatToDo.txt:0
./travel_guides/berlitz2/China-WhereToGo.txt:29
./travel_guides/berlitz2/Costa-History.txt:0
./travel_guides/berlitz2/Costa-WhatToDo.txt:0
./travel_guides/berlitz2/Costa-WhereToGo.txt:9
./travel_guides/berlitz2/CostaBlanca-History.txt:0
./travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:0
./travel_guides/berlitz2/Crete-History.txt:0
./travel_guides/berlitz2/Crete-WhatToDo.txt:2
./travel_guides/berlitz2/Crete-WhereToGo.txt:2
./travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:1
./travel_guides/berlitz2/Cuba-History.txt:0
./travel_guides/berlitz2/Cuba-WhatToDo.txt:0
./travel_guides/berlitz2/Cuba-WhereToGo.txt:7
./travel_guides/berlitz2/Nepal-History.txt:0
./travel_guides/berlitz2/Nepal-WhatToDo.txt:0
./travel_guides/berlitz2/Nepal-WhereToGo.txt:5
./travel_guides/berlitz2/NewOrleans-History.txt:1
./travel_guides/berlitz2/Paris-WhatToDo.txt:0
./travel_guides/berlitz2/Paris-WhereToGo.txt:17
./travel_guides/berlitz2/Poland-History.txt:0
./travel_guides/berlitz2/Poland-WhatToDo.txt:0
./travel_guides/berlitz2/Portugal-History.txt:0
./travel_guides/berlitz2/Portugal-WhatToDo.txt:0
./travel_guides/berlitz2/Portugal-WhereToGo.txt:10
./travel_guides/berlitz2/PuertoRico-History.txt:0
./travel_guides/berlitz2/PuertoRico-WhatToDo.txt:0
./travel_guides/berlitz2/PuertoRico-WhereToGo.txt:6
./travel_guides/berlitz2/Vallarta-History.txt:0
./travel_guides/berlitz2/Vallarta-WhatToDo.txt:0
./travel_guides/berlitz2/Vallarta-WhereToGo.txt:0
```
### Example 2 on File
```
[cs15lwi23apw@ieng6-201]:written_2:209$ grep -c "gardens" ./travel_guides/berlitz2/Canada-WhereToGo.txt 
11
```
* Explanation: print only a count of the number of lines that contain the pattern, instead of printing the matching lines themselves. The examples search up "garden" and "gardens," where it prints the file name in specified directory and the number of times the pattern appears in each file. It is useful, if the location isn't relevant but rather the number of times a word appears is (for instance counting percent A in a DNA sequence).
* Citation: used command `man grep` on terminal
