anagrammer
==========

Command line anagram generator written in Objective-C. The progam expects the following:

(1) An input dictionary text file with one word on each line. 
(2) An input text file of phrases to generate anagrams for, also one per line. 

To run from command line, type the following:

./anagrammer [pathToDictionary] [pathToPhrases]]

Ouput is in the following form:

moon starer = astronomer
debit card = bad credit,credit bad

Where the first word is per line is one of the input phrases, and the words after the equal sign are anagrams for that phrase. 

The anagrams are also ouput as JSON in the following format:

```javascript
{
  "anagramList": [
    {
      "anagrams": [
        "astronomer"
      ],
      "inputPhrase": "moon starer"
    },
    {
      "anagrams": [
        "bad credit",
        "credit bad"
      ],
      "inputPhrase": "debit card"
    }
  ]
}
```

Project includes a sample word dictionary (TWL06) sourced from here:

http://scrabblehelper.googlecode.com/svn/trunk/ScrabbleHelper/src/dictionaries/TWL06.txt

Project
==========

The Xcode project is organized as follows:

The __anagrammer__ target is essentially a wrapper around the static library anagrammerLib. 
The __anagrammerLib__ target contains the entirety of the program, including the main function and the associated classes for processing the dictionary and generating anagrams. 
The __anagarammerLibTests__ target inludes the unit tests for anagrammerLib. 

To run the unit tests in Xcode, simply select the __anagrammerLib__ scheme and select __Product-> Test__ (or type __Command-U__). 

 
