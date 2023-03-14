# Lab Report 5

## Lab Report 3 Remake but for find

## The -name command line option
The -name command line option finds a file in the directory with a specific search. It would be "find -name "`file pathway`" Which outputs 
the matching file.

In the example below we look for any file pathway that contains "WhereToGo.txt" at the end by using `*` In order to indicate the following pattern.

```
find  -name "*WhereToGo.txt"
./written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
./written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
./written_2/travel_guides/berlitz2/Athens-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bali-WhereToGo.txt
./written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt
./written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt
./written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
./written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
./written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
./written_2/travel_guides/berlitz2/California-WhereToGo.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
./written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
./written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
./written_2/travel_guides/berlitz2/Crete-WhereToGo.txt
./written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
./written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt
./written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt
./written_2/travel_guides/berlitz2/Paris-WhereToGo.txt
./written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
./written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```

In the next example, we do something similar to the previous example, however we can go even more specific to 
find the file that contains PuertoRico-WhereTo.txt.

```
find -name "*PuertoRico-WhereToGo.txt"
./written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
```

This command line option is helpful because it allows to search for a specific file name which comes in handy 
especially when trying to find out if a directory contains a file. Because if you used it correctly, nothing 
would be outputted if the file is not in the directory.

## The -empty command line option
The -empty command line option allows us to find empty directories or files. Empty directories do not contain 
files or subdirectories, and empty files do not contain data. 

In the following example I created a new directory called bruh, which has nothing inside of it we use the -empty 
accomponied by bruh/ to check if the bruh directory is empty. In which this is exactly what the -empty command line
option does.

```
find bruh/ -empty
bruh/
```
In the next example I wanted to see if the sub directory under written_2, non-fiction had any empty directories/files.
In this case, since nothing was outputted, there were no empty files/directories.

```
find non-fiction/ -empty
```

This command line option is helpful because it helps the user look for any empty directories/files that could be taking up
space in storage for no reason.


All commands found at [Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).
