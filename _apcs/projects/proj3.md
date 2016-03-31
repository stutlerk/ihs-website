---
layout: project
course: apcs

number: 3
title: A Gazillion Songs
due: 2016-04-21
turnin: #
forum: #

checkpoints:
  - title: Checkpoint 1 - Parsing Songs
    date: 2016-04-06
    value: 5%
    description: Have the Song class fully implemented and be able to parse input files.
  - title: Checkpoint 2 - Filtering and Sorting
    date: 2016-04-18
    value: 10%
    description: Be able to filter by at least one of the four fields and sort by at least one of the four fields.  
 

rubric:
  total: 50
  behavior:
    criteria:
      - criterion: Program greets the user on startup
        value: 1
      - criterion: Program prompts for input and output files
        value: 1
      - criterion: Program checks for missing input file and/or existing output file and responds accordingly
        value: 1
      - criterion: Output file format matches input file format
        value: 1
      - criterion: Program prompts for sort/filter command
        value: 1
      - criterion: Program is able to parse input file and create a SongCollection
        value: 2
      - criterion: Program is able to filter by artist
        value: 2
      - criterion: Program is able to filter by title
        value: 2
      - criterion: Program is able to filter by year
        value: 3
      - criterion: Program is able to filter by rank
        value: 3
      - criterion: Program is able to sort by any field
        value: 8
      - criterion: Program correctly handles multiple of same option in command
        value: 2
      - criterion: Program handles invalid commands gracefully
        value: 1
    total: 28
  implementation:
    criteria:
      - criterion: Range class is implemented as specified
        value: 1
      - criterion: Song class is implemented as specified
        value: 2
      - criterion: SongCollection class is implemented as specified
        value: 4
      - criterion: Program uses good style and is well-documented
        value: 3
      - criterion: Checkpoint 1
        value: 2
      - criterion: Checkpoint 2
        value: 5
      - criterion: Checkpoint 3
        value: 5
    total: 22
---
### Overview
Searching and sorting algorithms, such as those learned in class, are often used to manipulate and organize large datasets.  Among these types of datasets are lists of songs on either a user’s computer (through an application such as iTunes or xBox Music) or an internet service (such as Pandora or Spotify).  In this project, you will implement a text-based song database program that can sort or filter by various fields.

### Behavior

#### Program Operation
Upon startup, your program should greet the user and inform them that the program will sort and filter large databases of popular songs.  You should then prompt the user for an input file from which this database should be read.  A sample file [agazillionsongs.txt]({{site.baseurl}}\apcs\agazillionsongs.txt) that contains over 37,000 songs from the last 100+ years is provided for you to start with.

After the user provides the input file, you should ask them to enter a sort/filter command (see below) and an output file name.  Your program should then filter and sort the input song list according to the command and output the results to the specified file.  You must take your input in the following order: input file, sort/filter command, output file.  Each piece of input should be one line.  You should NOT have a loop to process multiple files—the program should terminate after the output has been printed to the specified output file. 


#### File Format
Input and output will be done to and from a file.  Both the input and output files should have the same format.  Each file will consist of a series of lines formatted as follows:
		Year\tRank\tArtist\tTitle

That is, each line of the file will consist of the year, rank, artist, and title of a single song, with each of the fields separated by tabs (\t).  Output files must maintain this format—you should be able to use the output file of one run of the program as the input to another run.

#### Entering Commands
A sort/filter command consists of one or more of the following options:
	
* -year:\<year(s)\>
* -rank:\<rank(s)\>
* -artist:\<artist\>
* -title:\<title\>
* -sortBy:\<field\>

Any number of these options may be given, and they may be given in any order.  If multiple options are specified, they will be separated by whitespace.  The details of these options are as follows:

* \<year(s)\> and \<rank(s)\> may be either a single number (e.g. 2002 or 1), or a range (e.g. 1998-2004 or 1-10).  Ranges should be in the form \<min\>-\<max\>.  To be valid, the max of a range must be greater than or equal to the min.
* \<artist\> and \<title\> may be either a full artist name or song title (e.g. “The Beatles” or “Thriller”) or a partial name or title (e.g. “Bob” or “Love”).  Artist names and song titles, including partials, should be enclosed in quotes.
* \<field\> must be one of the following: title, artist, year, or rank

If more than one instance of a single option is specified, the _last_ one entered should be used.  The entire sort/filter command should be entered on one line with options separated by spaces.  Here are some sample, valid sort/filter commands:

* -year:1990-1999 -rank:1-10
* -artist:john -sortBy:year
* -rank:1 -sortBy:artist
* -title:time
* -title:party -year:1985 -title:"the world"



#### Filtering
The -year, -rank, -artist, and -title options should cause the song list to be filtered according to the specified arguments.  For -year and -rank, only songs matching the specified value or falling within the specified range should be included in the output.  For -artist and -title, only songs that _contain_ the specified substring (case-insensitive) should be included.   Note that artists and titles need not match exactly—they only need to contain the specified string as a substring.

#### Sorting
The -sortBy option will cause the output to be sorted by a particular field.  If this option is specified, the output should be ordered according to the field named.  If there are ties, the tied songs should appear in same order in which they were in the input file.  If no -sortBy option is specified, the output should maintain the order of the input file.  


#### Extra Credit
You may earn extra credit by implementing additional features beyond those that are required.  Point values for extra credit features will be solely at my discretion and will be determined based on creativity and difficulty of implementation.  **No extra credit will be awarded for features that break required functionality, and points will still be lost for failing to meet requirements.**  It is HIGHLY recommended that you not attempt extra credit work until your project is fully complete.  Extra credit will be capped at 20% of the total project value.

Note that your extra credit work must not cause any of your unit tests to fail or otherwise cause the program functionality to change.  In other words, your extra credit features must not require the user to change their behavior to use the program properly-- you must simply add additional, optional features.


### Implementation Details

#### Required Classes
Your program must consist of four classes: **GazillionSongs**, **Song**, **SongCollection**, and **Range**.  GazillionSongs is the client, and should contain only the main method and other necessary helper methods.  The remaining classes should include the following methods, along with any other methods or fields you find necessary or useful:

|Song|
|---|---|
|public static Song parse(String s)|Parse a string of the form “Year\tRank\tArtist\tTitle” and create a Song object with the given values. |
|public int getYear()|Return the year of this song.|
|public int getRank()|Return the rank of this song.|
|public String getArtist()|Return the artist of this song.|
|public String getTitle()|Return the title of this song.|
|public String toString()|Return a string representation of this song.|

|SongCollection|
|---|---|
|public SongCollection(ArrayList<Song> songs)|Create a SongCollection containing the songs in the given ArrayList.|
|public void filterYear(Range r)|Remove all songs from this collection whose year does not match the given range.|
|public void filterRank(Range r)|Remove all songs from this collection whose rank does not match the given range.|
|public void filterArtist(String s)|Remove all songs from this collection whose artist does not contain the given string (case-insensitive).|
|public void filterTitle(String s)|Remove all songs from this collection whose title does not contain the given string (case-insensitive).|
|public void sortYear()|Order the songs in this collection by year (ascending).|
|public void sortRank()|Order the songs in this collection by rank (ascending).|
|public void sortArtist()|Order the songs in this collection lexicographically by artist (ascending, case-insensitive).|
|public void sortTitle()|Order the songs in this collection lexicographically by title (ascending, case-insensitive).|
|public String toString()|Return a string representation of this collection—the string representation of each Song, in the current order, separated by newlines.|

|Range|
|---|---|
|public static Range parse(String s)|Parse a string of the form "<min>-<max>" or "<value>" and create a Range representing those values|
|public boolean contains(int n)|Returns true if the given value is in this range, and false otherwise.|
|public int getMin()|Return the minimum value in this range.|
|public int getMax()|Return the maximum value in this range.|

#### Error Checking
Your program should not crash as long as the user provides reasonable input.  You may assume that the input file is correctly formatted.  However, your program must be able to handle other error conditions, _including but not limited to_:

* input file does not exist
* output file already exists (confirm overwrite)
* some option appears more than once in sort/filter command
* unrecognized option given in sort/filter command
* range specified for -year or -rank is invalid

In these (and any other) error cases, your program should recognize and report the error, then exit gracefully.
