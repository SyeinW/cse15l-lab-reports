# Lab Report 3
## grep command-line options

### grep -n
Usage: ```grep -n``` returns the line number that contains the text pattern, followed by the line itself. It does this for every line that contains the text pattern.
Citation: grep --help & [grep wiki books](https://en.wikibooks.org/wiki/Grep)

```
$ grep -n "Germany" written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt 
14:More than just a department store, KaDeWe (Kaufhaus des Westens), located on the edge of Wittenbergplatz, has achieved the status of a monument since its foundation in 1907. The food emporium on the sixth floor is extraordinary. Here, gourmet globetrotters can perch on a bar stool and sample not only food from all over Germany but also Chinese, Japanese, Russian, French, and Swiss cuisine. One floor up, the Wintergarten is a vast food court in the glass-roofed atrium where shoppers can help themselves to less exotic, but equally tasty fare. It’s an ideal spot for a hearty breakfast before a day’s shopping. The toy department is also well worth a visit.
36:A few minutes’ walk from the Kongreßhalle you’ll find the Reichstag building, its huge, new glass dome, with its mirrored central funnel, visible from much of the city. The parliamentary home of Wilhelminian and Weimar Germany displays the proud dedication Dem deutschen Volke (To the German People) on a Neo-Classical façade built in 1894 by Paul Wallot. This appeal to patriotism and democracy, set above six Corinthian columns, outlasted the burning in 1933 and the bombs of World War II, and was given renewed significance when Berlin resumed its former role as the seat of government of a unified Germany. Today, the dome is a major attraction for Berliners and tourists alike. They endure lengthy lines to be able to travel to the top, gazing out at the city and down into the Bundestag chamber. By the end of 2003, the area in front of the Reichstag — currently a vast construction site — will be transformed, with the completion of all the new government district buildings, including the Federal Chancellery. An enormous new Berlin Central Train Station is being erected at Lehrter Bahnhof, and new S– and U–bahn 
lines are being built, to further extend the city’s already splendid public transport system.
54:The area east of the Brandenburg Gate known as Mitte (Middle) is the historic center of Berlin, and was at one time the center of the capital of the German Democratic Republic. The city’s most important museums, theaters, 
government buildings, and churches were constructed here between the 18th and 20th centuries. Many buildings, including the Friedrichswerdersche Kirche (now home to the Schinkel-Museum, see page 58) and Schinkel’s Altes Museum (Old Museum; see page 76), were carefully restored by East Germany after air-raid bombing of World War II, and several quarters were rebuilt in the Old Berlin style, notably Gendarmenmarkt (formerly Platz der Akademie) and 
Museumsinsel (see page 76).
73:Step inside the Französischer Dom to visit the Huguenot museum, or look up the stairwell to the Glockenspiel — a dizzying 48 m (159 ft) above. The Turmstuben restaurant on the fourth floor is the place to calm your shattered nerves. The Deutscher Dom now houses a fascinating exhibition, Fragen an die deutsche Geschichte (German History Under Question), which was previously in the Reichstag. This frank examination of Germany’s social and political history cleverly combines documents, photographs, and radio broadcasts to chronicle the rise of Fascism and the development of democracy. The descriptive panels are all in German, but audio guides and information booklets are available in English and French.
78:On the north side of the River Spree, Oranienburger Straße is the heart of the old Jewish quarter. In the 1920s, a diverse community of Jewish professionals and Bohemian artists and writers lived, worked, and thrived here. After the devastation of the war and the grim sterility of its aftermath, the area has now regained much of its former vibrancy, with cultural centers and Jewish restaurants rubbing shoulders with off-beat cafés and alternative art venues beneath the magnificent black-and-gold-leafed dome of the Neue Synagogue. The biggest synagogue in Germany, designed by Eduard Knoblauch and completed in 1866, it was gutted during the anti-Semitic attacks of Kristallnacht on 9 November 1938 (see page 21) and then later destroyed by Allied bombing. It has now been beautifully restored, and is used for services once more. In addition, exhibits from the adjacent center of Jewish studies, Centrum Judaicum, are displayed here.
82:The palace balcony from which Spartacist leader Karl Liebknecht proclaimed his doomed “Socialist Republic” in 1918 was added to the front of the Staatsrat (Council of State) building on the east side of the square, while the monstrous bronze, glass, and steel Palast der Republik, once, not so very long ago, the seat of East Germany’s parliament, replaced what remained of the royal residence. Recent budget cuts have postponed the demolition of 
the Palast, and there is a movement afoot to preserve it as an historic monument.
120:Königsstraße extends as far as an illustrious relic of the Cold War, Glienicker Bridge, once a restricted border crossing between West Berlin and East Germany where the KGB and CIA exchanged spies.
146:The new wing of Schloß Charlottenburg provides a fine setting for works by 19th-century Romantic painters, and boasts the most comprehensive collection of paintings by Caspar David Friedrich to be found in Germany. Among 
his works, look for Abtei im Eichwald (Abbey in the Woods, 1809) and Der Mönch am Meer (The Monk by the Sea, 1810).
184:This fascinating new museum commemorates Berlin’s history as the Hollywood of Germany and, in a remarkable display featuring items from her personal estate, pays tribute to the greatest of all German screen stars, Marlene Dietrich.
233:Beside the lake, north of the town center is Neuer Garten, a pleasant English-style garden. It provides the perfect setting for Schloß Cecilienhof (1916), the ivy-covered, half-timbered pastiche of an English country manor built for Crown Prince Wilhelm and his wife. Winston Churchill, Joseph Stalin, and Harry Truman met here in July 1945 to draw up the Potsdam Agreement that fixed the division of Germany for the next 45 years. Today it’s a luxury hotel and restaurant.
```


The `-n` command line option prints the lines that have the specified pattern (`Germany` in this case) and their line number. This is useful for finding the exact line number where the pattern orginates. Could be useful for citations and quick searching for quotes. 

```
$ grep -n "Lucayans" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt:6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```


The command line option `-n` is doing the exact same thing as it was in example 1, except we are giving a slightly different argument. In this case, we don't defined a specific `.txt` file for it to look at. Instead, we give it a directory and then use `*.txt` to search every txt file in the `berlitz2` directory for the pattern `Lucayans` 

### grep -l
Explanation: ``` grep -l``` returns the names of the files that contain the pattern instead of the lines.
Citation: grep --help & [grep wiki books](https://en.wikibooks.org/wiki/Grep)

```
$ grep -l "Germany" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Algarve-History.txt
written_2/travel_guides/berlitz2/Amsterdam-History.txt
written_2/travel_guides/berlitz2/Athens-History.txt
written_2/travel_guides/berlitz2/Bali-History.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/Berlin-History.txt
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
written_2/travel_guides/berlitz2/Budapest-History.txt
written_2/travel_guides/berlitz2/Canada-History.txt
written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/CostaBlanca-History.txt
written_2/travel_guides/berlitz2/Poland-History.txt
written_2/travel_guides/berlitz2/Portugal-History.txt
```


The command line option `-l` is causing the terminal to print out the files containing the pattern `Germany`. This is useful when you only want to know if a file contains the pattern, rather than actually seeing the whole line. If we used ```grep``` our terminal would have been overrun with hundreds of lines, by using ```grep -l``` we are able to look solely at which paths contain the pattern. Going back to the `-n` command line option, if we didn't know how to use `*.txt`(example 2 of `-n`) this would be a good way to find every file that we could run with the `-n` to get an output (example 1 of `-n`). 

``` 
$ grep -l "English" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Algarve-History.txt
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
written_2/travel_guides/berlitz2/Amsterdam-History.txt
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
written_2/travel_guides/berlitz2/Athens-History.txt
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Bali-History.txt
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
written_2/travel_guides/berlitz2/Bermuda-history.txt
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
written_2/travel_guides/berlitz2/Budapest-History.txt
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt
written_2/travel_guides/berlitz2/California-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-History.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/Costa-History.txt
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
written_2/travel_guides/berlitz2/Cuba-History.txt
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt
written_2/travel_guides/berlitz2/NewOrleans-History.txt
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
written_2/travel_guides/berlitz2/Portugal-History.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
written_2/travel_guides/berlitz2/PuertoRico-History.txt
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
```


Same reasoning as example 1 of `-l`

### grep -c
Explanation: Terminal will return the path followed by the number of times pattern appeared within that specific input file.
Citation: grep --help & [grep wiki books](https://en.wikibooks.org/wiki/Grep)

``` 
$ grep -c "English" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Algarve-History.txt:1
written_2/travel_guides/berlitz2/Algarve-Intro.txt:0
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Amsterdam-History.txt:3
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt:1
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt:3
written_2/travel_guides/berlitz2/Athens-History.txt:1
written_2/travel_guides/berlitz2/Athens-Intro.txt:0
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bahamas-History.txt:4
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:3
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:5
written_2/travel_guides/berlitz2/Bali-History.txt:1
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Barcelona-History.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Beijing-History.txt:0
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt:6
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt:3
written_2/travel_guides/berlitz2/Berlin-History.txt:0
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt:2
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt:5
written_2/travel_guides/berlitz2/Bermuda-history.txt:4
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt:2
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:3
written_2/travel_guides/berlitz2/Budapest-History.txt:1
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt:2
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt:3
written_2/travel_guides/berlitz2/California-History.txt:0
written_2/travel_guides/berlitz2/California-WhatToDo.txt:0
written_2/travel_guides/berlitz2/California-WhereToGo.txt:1
written_2/travel_guides/berlitz2/Canada-History.txt:6
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:26
written_2/travel_guides/berlitz2/CanaryIslands-History.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Cancun-History.txt:0
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt:2
written_2/travel_guides/berlitz2/China-History.txt:0
written_2/travel_guides/berlitz2/China-WhatToDo.txt:0
written_2/travel_guides/berlitz2/China-WhereToGo.txt:6
written_2/travel_guides/berlitz2/CostaBlanca-History.txt:0
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Costa-History.txt:1
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Crete-History.txt:0
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt:1
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Cuba-History.txt:1
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Nepal-History.txt:0
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:0
written_2/travel_guides/berlitz2/NewOrleans-History.txt:1
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:2
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:3
written_2/travel_guides/berlitz2/Poland-History.txt:0
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt:2
written_2/travel_guides/berlitz2/Portugal-History.txt:2
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:6
written_2/travel_guides/berlitz2/PuertoRico-History.txt:2
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Vallarta-History.txt:0
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:0
```


The command line option `-c` prints out how many lines per file are matching the pattern `English`. grep -c is useful when we don't care where the pattern occurs within the text file, but how many times it occurs. Ex: we want to have 4 if statements in a text file, but there is an arbitrary large amount of lines of code, we can use ```grep -c``` to make sure there are only 4 if statements. We can also use it for data collection, as if we wanted to know how many times the word "one" occured, it is much easier to read the path name + the occurence number, then something like grep -n where we have to seen the entire line. 

```
$ grep -c "Biosphere" written_2/non-fiction/OUP/Kauffman/*.txt
written_2/non-fiction/OUP/Kauffman/ch1.txt:3
written_2/non-fiction/OUP/Kauffman/ch10.txt:0
written_2/non-fiction/OUP/Kauffman/ch3.txt:0
written_2/non-fiction/OUP/Kauffman/ch4.txt:0
written_2/non-fiction/OUP/Kauffman/ch5.txt:0
written_2/non-fiction/OUP/Kauffman/ch6.txt:1
written_2/non-fiction/OUP/Kauffman/ch7.txt:1
written_2/non-fiction/OUP/Kauffman/ch8.txt:2
written_2/non-fiction/OUP/Kauffman/ch9.txt:0
```


Same reasoning as example 1 of `-c`

### grep -w
Explanation: ```grep -w``` returns lines that have the exact pattern, so if the pattern x is a root word for another word y, then the word y would not be displayed in the terminal. 
Citation: grep --help & [grep wiki books](https://en.wikibooks.org/wiki/Grep)


``` 
$ grep -w "German" written_2/travel_guides/berlitz2/Berlin-History.txt 
The German capital became a municipality during the 1200s, ironically as a divided city. In those days the two rival halves were in no rush to unite. The fishermen of Cölln, whose name survives in the modern borough of Neukölln, lived on an island in the River Spree. The townships that comprise the modern Mitte district grew up around market places over which the people’s churches, the Nikolaikirche and Marienkirche, still tower today. With the fortress of Burg Köpenick providing a common defense to the south, Cölln and Berlin formed a trade center between Magdeburg and Poznan.
In a region inhabited by the Slavonic Sorbs, the population of the city was overwhelmingly German by the 13th century, comprising enterprising merchants hailing from the northern Rhineland, Westphalia, and Lower Saxony, with 
latecomers from Thuringia and the Harz. Berlin and Cölln came together in 1307 in order to lead the Brandenburg region’s defenses and defeat the robber barons who were terrorizing merchants and local peasants. The prosperous 
city joined the Hanseatic League, trading in rye, wool, and oak timber and providing an entrepôt for skins and furs from eastern Europe. Apparently living was easy in the 15th century, as historian Trithemius noted: “Life here consists of nothing but eating and drinking.”
Berlin continued as a virtually autonomous outpost of the German empire until 1448, when Brandenburg’s Kurfürst (Prince Elector) Friedrich II took over control of the city after crushing the citizens’ violent resistance, the 
so-called Berliner Unwillen. He was a member of the Hohenzollern dynasty that was to hold sway here for over 450 years.
The independent spirit of the Berliners was felt during the Reformation in the 16th century. The people were tired of paying the tribute exacted by the Catholic church. In 1539, at a time when citizens of the other German principalities had to observe the religion of their prince, Berliners were successful in pressuring Prince Elector Joachim II to accept the Protestant creed as preached by Martin Luther.
Friedrich der Große (Frederick the Great, 1740–1786), King of (not just in) Prussia, took his realm to the forefront of European politics and had little time for Berlin. He concentrated on turning his beloved Potsdam into a mini-Versailles, where French was spoken and Voltaire became his official philosopher-in-residence. He rarely appeared in Berlin except to garner public support — and taxes — after his return from costly wars with the Silesians, Russians, and Austrians. He did, nevertheless, leave the German capital an enduring legacy with the monumental Forum Fridericianum laid out on Unter den Linden by his architect von Knobelsdorff.
The armies of Frederick’s successors proved to be no match for Napoleon’s Grande Armée, however, and as the French advanced through eastern Germany in 1806, Berlin’s bureaucracy, court, and bourgeoisie fled to the country. No troops were left to defend the city from its invaders, and Napoleon’s march through the Brandenburg Gate into Berlin kindled a new flame of German patriotism.
Defying the two-year French occupation, philosopher Johann Gottlieb Fichte exhorted the German people to assume their rightful destiny as a nation. Drummers were ordered to drown out his fiery speeches at the Royal Academy.  
After that philistine period of rapid growth, the city at last began to assume its place as Germany’s cultural as well as political capital, with Berlin artists Max Liebermann, Lovis Corinth, and Max Slevogt challenging Munich’s dominance of German painting. The Berlin Philharmonic asserted an international prestige, attracting Tchaikovsky, Strauss, and Grieg as guest composers, and in 1905, the great Viennese director Max Reinhardt arrived to head the Deutsches Theater.
Privations at home and the horrendous loss of life on the front turned popular feeling against the war. In 1916, Karl Liebknecht and Rosa Luxemburg formed the Spartacus League. Two years later, with Germany defeated and insurrections in Kiel, Munich, Hamburg, and Stuttgart, revolution broke out in Berlin. While the Social Democrats were proclaiming a new German Republic, Liebknecht took over the palace declaring the Republic socialist, with “supreme authority for the workers and soldiers.”
The conservative establishment winced when the Prussian Writers’ Academy chose as its president Heinrich Mann, the elder brother of Thomas Mann, a violent critic of the German bourgeoisie and supporter of the Communist Party. His best-known novel, Professor Unrat, inspired Josef von Sternberg’s The Blue Angel, the film that revealed the vocal talents of Marlene Dietrich.
Berlin was going through a wild time, but the Versailles peace treaty had laid heavy burdens on the nation. At the start of the twenties, inflation had made little more than nonsense of the German currency, and political assassinations became routine. The most significant of the victims was foreign minister Walther Rathenau, an enlightened democrat and Jew who was killed near the Grunewald forest. It was also the time of vicious street battles between Communists and Nazis, exploiting the social disruptions of inflation and unemployment that were impossible to ignore.
Communist hostility towards the Social Democrats split the opposition to the Nazis. Hitler became Chancellor on 30 January 1933. Only a month later, on 27 February, the Reichstag went up in flames. Hitler used the fire as a pretext to eliminate Communist and all left-wing opposition from German political life. The Nazi reign of terror had begun.
Discrimination against Jews moved inexorably to the night of 9 November 1938, when synagogues and other Jewish-owned buildings were burned. In the midst of the smashed glass of the looted shops, German wit eased the discomfort by referring to the event as Kristallnacht (Crystal Night). Berlin’s Jewish population, which stood at 170,000 in 1933, was reduced by emigration and extermination to around 6,000 by 1945.
Their disquiet was shortly to be justified by the hail of bombs on the capital. The first attacks came in 1940 from the British in retaliation for the air raids on London. Attacks were stepped up after the German defeat at Stalingrad in 1943, with Anglo-American “carpet-bombing.” The worst single raid was on 6 February 1945, when bombs wiped out 4 sq km (1 1⁄2 sq miles) of the city center in one hour.
The war ended with unconditional German surrender on 8 May 1945. In Berlin, the population was left to pick up the pieces — literally. Women formed groups of Trümmerfrauen (rubble women), with 60,000 of them passing the debris of war by hand to clear ground for rebuilding. Eventually there was sufficient rubble to create a few artificial mountains. One of them, Teufelsberg in the Grunewald, is big enough to ski on.
Hard political realities soon developed from these administrative divisions, as the Allies found themselves confronted with Soviet efforts to incorporate the whole of Berlin into a new Communist-controlled German Democratic Republic. In the 1946 municipal elections — Berlin’s first free vote since 1933, and its last until 1990 — the Social Democrats won a crushing victory over the Communists, prompting the Soviets to tighten their grip on the eastern sector. Understandably unhappy that West Berlin’s capitalist presence in the middle of East Germany was having a subversive influence on the Communist experiment, the Soviets and their East German allies began to restrict traffic from West Germany. In June 1948, all road, rail, and waterway routes to West Berlin were sealed off. From bases in Frankfurt, Hamburg, and Hanover, the Western Allies countered the blockade by airlifting into Berlin between 4,000 and 8,000 tons of food and other vital supplies every day for 11 months. The blockade finally ended in May 1949, and West Berlin became a Land linked administratively with, but thus far not politically incorporated into, the new Federal Republic of Germany. East Berlin was made capital of the fledgling German Democratic Republic.
In the early hours of 13 August 1961, East German workers and soldiers began to erect the wall that would separate East and West Berlin and change the lives of several million people for nearly 30 years. The wall started out 
as barbed wire and road blocks, but refugees continued to make their way through the barriers, by swimming through sewers and canals and jumping from buildings and railway bridges — risking life and limb for freedom and democracy. Soon, huge slabs of reinforced concrete and tank-traps formed a more impenetrable barrier. Crossing points were established for foreigners and for West Germans, but not for Berliners, until a tiny few were allowed across much later in the Cold War confrontation.
The erection of the Wall did significantly reduce the flow of refugees to a few isolated escapes, but the East German economy suffered even more from the assaults of massive mismanagement and high-level corruption. Erich Honecker’s regime won international diplomatic recognition for East Berlin as its capital and, with gleaming hotels and skyscrapers, tried to give it a lustre to rival West Berlin. Beneath the surface, however, the drabness of daily life and lack of personal freedom continued to undermine any chance of popular support.
The final push which led to the collapse of the Berlin Wall came when an ecological campaign in Leipzig against nuclear weapons and industrial pollution grew into nationwide pressure for democratic freedom. In 1989, with thousands of East Germans fleeing to the West via Hungary, Czechoslovakia, and Poland, the country was swept up in the wave of eastern European revolutions unleashed by the reforms of Soviet leader Mikhail Gorbachev. His visit to East Berlin in October 1989 for the 40th anniversary of the German Democratic Republic left it clear that Soviet troops would no longer shore up its regime. The Berlin Wall was opened on 9 November 1989, and at midnight on 3 October 1990, a huge black, red, and gold national flag was hoisted at the Reichstag. East and West Berlin were again one.
On 20 June 1991, the city’s role at the hub of German life was assured when the Bundestag voted by a slim majority to restore Berlin as the seat of government. In May 1999 a federal President was elected at the Reichstag and, in August that year, government business again began to be conducted from Berlin. The Reichstag was transformed by the addition of a vast glass dome, designed by Sir Norman Foster, to symbolize that the new Germany keeps no 
secrets from its people. 
``` 


The `-w` command line option makes it so the pattern `German` has to match exactly with the words in the `.txt` files in order to be printed to the terminal. If we didn't put the `-w`, Germany could have been a possible word that triggered pattern. This is extremely useful for differentiating specific words that are roots of other words. 


``` 
$ grep -w "judge" written_2/*/*/*.txt
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:        contests judge competitors on their most spectacular flying
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:        the grave of the 15th-century Muslim judge and historian, Mujr el-Din.
written_2/travel_guides/berlitz1/WhereToMadeira.txt:        in itself. Madeira’s microclimates are very difficult to judge,
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:Olhão has often been described as the “little white Cubist town of the Algarve,” its architecture likened to that of North African towns. That may have been the case some years ago, but modern development has strongly interfered with its once distinctive appearance. You can judge for yourself by ascending the bell tower of the parish church (which also goes by the name of Nossa Senhora do Rosário), which you will find by winding your way through the narrow streets back to the Praça da Restauração (you may have to ask for access to the tower in the sacristy). Founded by King Dom Pedro II in 1698, the church has an impressive, scroll-decorated Baroque façade, brilliant white dome, stone belltower, and a chapel at the rear, Nossa Senhora dos Aflitos (Our Lady of the Afflicted), where women often pray when their fishermen husbands are away at sea.
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt:Paintings: If you want a unique work of art, you’ll need to study the field. Visit the major collections to judge the standard of the best paintings, especially the Neka Museum and Museum Puri Lukisan in Ubud (see page 41) as well as the Arts Centre in Denpasar (see page 37). Don’t just assume that a high price guarantees original work.
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt:West of Klungkung, a narrow lane leads to the village of Tihingan, one of only two places in Bali where the gongs for gamelan orchestras are made. The other is Sawan, near the north coast (see page 65). In any of the bronze foundries, you’ll find the same medieval scene, with a boy apprentice pumping the bellows to keep a charcoal fire blazing while the smiths hammer away. Hanging mats keep the 
place in semi-darkness so that the workers can judge the temperature of the glowing metal by its color. In the village of Banda, about 5 km (3 miles) south of Tihinga, a museum celebrates one of Bali’s most successful contemporary artists, Nyoman Gunarsa.
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt:Jade. China’s most prized precious stone is also quite difficult to judge. Unless you are with an expert, buy only what you like at a price you can easily afford. Some jade is fake. Color, transparency, smoothness, and the skill of cutting determine the price. Check the Friendship Store first to see what you get for your money.
```

Same reasoning as example 1 of `-w`
