# Lab Report 3
## grep command-line options

### grep -n
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

The ` -n ` command line option prints the lines that have the specified string (`Germany` in this case) and their line number. This is useful for finding the exact line number where the string argument orginates. Could be useful for citations and quick searching for quotes. 

```
$ grep -n "Lucayans" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt:6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

The command line option ` -n ` is doing the exact same thing as it was in example 1, except we are giving a slightly different argument. In this case, we don't defined a specific `.txt` file for it to look at. Instead, we give it a directory and then use `*.txt` to search every txt file in the `berlitz2` directory for the string argument `Lucayans` 

### grep -l
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

The command line option ` -l ` is causing the terminal to print out the files containing the string argument `Germany`. This is useful for finding which files contain the word you are looking for. Going back to the ` -n ` command line option, if we didn't know how to use `*.txt`(example 2 of `-n`) this would be a good way to find every file that we could run with the ` -n ` to get an output (example 1 of `-n`). 

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

### grep -c
Citation: grep --help & [grep wiki books](https://en.wikibooks.org/wiki/Grep)

``` ```

What its doing and why its useful

``` ```

What its doing and why its useful

### grep -o
Citation: grep --help & [grep wiki books](https://en.wikibooks.org/wiki/Grep)

``` ```

What its doing and why its useful

``` ```

What its doing and why its useful
