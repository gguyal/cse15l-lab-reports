# Lab Report 3
## The -l command line option
The -l command line option outputs the matching files that contains the specific string searched for in a given path. 
This is useful when looking for a file that contains a specific string.

```
grep -rl "Lucayans" written_2
written_2/travel_guides/berlitz2/Bahamas-History.txt
```

The previous example also implements the **-r** command line option which allows us to search through directories recursively.
The **-l** command line follows **-r** so that it outputs the file within the directory.
In this example we search for the string "Lucayans" within the directory written_2. using -rl, in order to output the file containing
the string.

```
grep -rl "Canada" written_2
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch9.txt
written_2/non-fiction/OUP/Kauffman/ch3.txt
written_2/non-fiction/OUP/Rybczynski/ch2.txt
written_2/non-fiction/OUP/Rybczynski/ch3.txt
written_2/travel_guides/berlitz1/HandRJamaica.txt
written_2/travel_guides/berlitz1/HandRMadrid.txt
written_2/travel_guides/berlitz1/HistoryFWI.txt
written_2/travel_guides/berlitz1/HistoryHawaii.txt
written_2/travel_guides/berlitz1/HistoryHongKong.txt
written_2/travel_guides/berlitz1/HistoryJapan.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz2/Bermuda-history.txt
written_2/travel_guides/berlitz2/California-WhatToDo.txt
written_2/travel_guides/berlitz2/Canada-History.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/NewOrleans-History.txt
```

In this example we are using the same command line of -rl in order to search through the directory written_2 and return the matching files
that contain our given string "Canada".

## The -i command line option
When we would usually search for a string, the string has to be fully case-sensitive meaning that all characters, capitals, or lowercase 
has to be the exact same.
When we use the -i command line option, we still have to contain the same characters, however, we are able to ignore any uses of capitals 
or lowercase and just searches for its matching letters in the order given.
This would be useful in the case where you are looking for any cases of the word, eg. if you were to search for "Chicken" it would bring up
both the capital and lower of "c". To me it is similar to the "Ctrl-f" function in a web browser.

```
grep -i "CANADA" findresults.txt
./written_2/travel_guides/berlitz2/Canada-History.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```

In the example above, findresults.txt is a text file that contains all of the .txt files from written_2 directory. We search for the string
"CANADA" using the -i command line, and since we used -i , this ignores all cases of lowercase and capitals, and still outputs the location
of any combination of capitals/lowercase of the string "CANADA".

```
grep -i "hIstOry.tXT" findresults.txt
./written_2/travel_guides/berlitz2/Algarve-History.txt
./written_2/travel_guides/berlitz2/Amsterdam-History.txt
./written_2/travel_guides/berlitz2/Athens-History.txt
./written_2/travel_guides/berlitz2/Bahamas-History.txt
./written_2/travel_guides/berlitz2/Bali-History.txt
./written_2/travel_guides/berlitz2/Barcelona-History.txt
./written_2/travel_guides/berlitz2/Beijing-History.txt
./written_2/travel_guides/berlitz2/Berlin-History.txt
./written_2/travel_guides/berlitz2/Bermuda-history.txt
./written_2/travel_guides/berlitz2/Budapest-History.txt
./written_2/travel_guides/berlitz2/California-History.txt
./written_2/travel_guides/berlitz2/Canada-History.txt
./written_2/travel_guides/berlitz2/CanaryIslands-History.txt
./written_2/travel_guides/berlitz2/Cancun-History.txt
./written_2/travel_guides/berlitz2/China-History.txt
./written_2/travel_guides/berlitz2/Costa-History.txt
./written_2/travel_guides/berlitz2/CostaBlanca-History.txt
./written_2/travel_guides/berlitz2/Crete-History.txt
./written_2/travel_guides/berlitz2/Cuba-History.txt
./written_2/travel_guides/berlitz2/Nepal-History.txt
./written_2/travel_guides/berlitz2/NewOrleans-History.txt
./written_2/travel_guides/berlitz2/Poland-History.txt
./written_2/travel_guides/berlitz2/Portugal-History.txt
./written_2/travel_guides/berlitz2/PuertoRico-History.txt
./written_2/travel_guides/berlitz2/Vallarta-History.txt
```

The above example shows the **-i** still working even after the different combinations of capitals and lowercase, as well as an inclusion
of characters outside of letters.


## The -n command line option
The -n command line outputs the matching line that contains the searched string as well as it's line number.
The reason this is useful, is because if you ever wanted to know the location within the file where the string is at, this command line out-
puts it.

```
grep -n "Canada" findresults.txt
185:./written_2/travel_guides/berlitz2/Canada-History.txt
186:./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```

The examples above uses the -n command line searching for "Canada" in the findresults.txt file and shows the line where the string is at,
well as its line numbers which are 185 and 186.

```
grep -rn "Lucayans" written_2
written_2/travel_guides/berlitz2/Bahamas-History.txt:6:Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
written_2/travel_guides/berlitz2/Bahamas-History.txt:7:The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```
This example shows us using the -r command with the modifier of the -n as well as -o. We are allowed to search through the directory written_2.
And then we are able to output the line that Lucayans was found at within its text files, which is at 6 and at 7, however you can see this method
makes it difficult to actually read. So, in the next command line mentioned, we are going to show how we can actually bypass showing the entire 
text file, so we can identify the line number easier.


## The -o command line option
The -o command line option outputs the matching part of the line.
This is useful when combined with other modifiers!

```
grep -rno "Lucayans" written_2
written_2/travel_guides/berlitz2/Bahamas-History.txt:6:Lucayans
written_2/travel_guides/berlitz2/Bahamas-History.txt:7:Lucayans
```

This is similar to a previous example mentioned, however we use -o as a modifier. By using this command line we are able to only locate the matched
part in the line, and then output the line number, which is at 6 and 7. This is useful as it eliminates any unnecessary texts outputted.

```
grep -ino "CANADA"  findresults.txt
185:Canada
186:Canada
```

In this example we are using -i to ignore all cases of capitals and lowercases, as well as the line number, and just the matched output value. This is 
useful, if you were to search for a word but just wanted the word, and wanted to know its line number, while ignoring all the extra text outputs you may
receive if you ran this command without **-o**.

All commands found at [Link](https://en.wikibooks.org/wiki/Grep).
