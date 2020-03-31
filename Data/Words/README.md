# Words

## Objective
Obtain the top 10 words in a long text (book), sorted by the number of appearances. The faster implementation wins.

Entry candidates are any valid program, compiled or interpreted that targets Linux on a Raspberry Pi 3, as the platform of choice to profile the solution. Use any programming language, library or tool.

## License
Each author retains the rights to his/her code, but each entry shall have a OSI approved license in order to be considered for participation.

## Conditions
- The entry shall work on any text with UTF-8 encoding. As an example, a long book in the Public Domain is available: [Don Quijote de la Mancha](http://www.gutenberg.org/cache/epub/2000/pg2000.txt) (Spanish, book 2000, Project Gutenberg) in order to test the suitability of the algorithm.
- Spanish was choosen to verify the correctness of the implementation beyond ASCII range. The search is case insensitive.
- Discard articles, conjunctions and propositions from the list. You don't need to know spanish, discard_es.txt is the list of words to be discarded.
- Discard numeric entities or words mixed with numbers.
- Each entry shall be produced directly from source. Any optimization is permitted but executable compression is not allowed.
- There is a penalty of 1 ms for each kb needed to execute the entry. This puts in disadvantage the interpreted languages with respect to native compiled solutions. For instance: a shell script will carry the size of the minimal shell required to run it.
- The entry that obtain the right solution faster than the reference implementation will receive a prize.

## Results
The current performance of the reference implementation in a Raspberry Pi 3 Model B Rev 1.2 is:
```sh
$ time ./rds pg2000.txt
0.  "no" 6345
1.  "se" 4691
2.  "su" 3352
3.  "don" 2652
4.  "me" 2345
5.  "quijote" 2180
6.  "sancho" 2148
7.  "es" 2142
8.  "yo" 2077
9.  "más" 2044

real    0m10,645s
user    0m10,558s
sys     0m0,040s
```
The penalty is: 1027 kb -> 1.027 s.

Total performance for the reference implementation: 11.585 seconds (This is the mark to beat)
