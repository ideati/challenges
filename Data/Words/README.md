# Words

## Objective
Obtain the entire list of words in a long text (book), sorted by the number of appearances. The faster implementation wins.

## License
Each author retains the rights to his/her code, but each entry shall have a OSI approved license in order to be considered for participation.

## Restrictions
- The entry shall work on any spanish text with UTF-8 encoding. A long book in the Public Domain is available: [Don Quijote de la Mancha](http://www.gutenberg.org/cache/epub/2000/pg2000.txt) in order to test the suitability of the algorithm.
- Discard articles, conjunctions and propositions from the list.
- Discard numeric entities or words mixed with numbers.
- Use any programming language and any free library and/or tool.
- The resulting program could be compiled or interpreted but shall run on a Raspberry Pi 3, as the platform of choice to profile the solution.
- Each entry shall be produced directly from source. Any optimization is permitted but executable compression is not allowed.
- There is a penalty of 1 ms for each kb needed to execute the entry. This puts in disadvantage the interpreted languages with respect to native compiled solutions. For instance: a shell script will carry the size of the minimal shell required to run it.
- The entry that obtain the right solution faster than the reference implementation will receive a prize.
