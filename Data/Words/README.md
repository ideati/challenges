# Words

## Objective
Obtain the top 10 words in a long text (book), sorted by the number of appearances. The faster implementation wins.

A valid entry is any program, compiled or interpreted and able to run on a [Raspberry Pi 3](https://www.raspberrypi.org/products/raspberry-pi-3-model-b/), as the platform of choice to profile the solution. Use any programming language, library or tool. The code should be portable, at least between x86_64 and ARM platforms. You don't need to have a RPi, it will be used just to determine the speed with respect to the reference implementation. The entry that obtain the right solution faster than the reference implementation will receive a [prize](https://github.com/ideati/challenges/blob/master/PRIZE.md). The reference implementation will be revealed once the contest ends. 

## Deadline
This challenge goes up to june 30, 2020. The final results will be published here on saturday, july 18, 2020.

## License
Each author retains the rights to his/her code, but each entry shall have a OSI approved license in order to be considered for participation.

## Conditions
- The entry shall work on any text with UTF-8 encoding. As an example, a long book in the Public Domain is available: [Cervantes' Don Quijote de la Mancha, 2.2MB](http://www.gutenberg.org/cache/epub/2000/pg2000.txt) (Spanish, Project Gutenberg Book No.2000) in order to test the suitability of the algorithm. This book has 23.591 different words for a total of 384.324 words. By the way: it's such a wonderful book, reading it is a prize on itself!
- A spanish book was chosen to verify the correctness of the implementation beyond the ASCII range, something of crucial importance for the correctness of our platform.
- The search is case insensitive and all orthographic marks shall be taken into account: "más" != "mas", "Éxito" == "éxito". 
- Discard articles, conjunctions and propositions from the list. You don't need to know spanish to do it. There is a list of the words to be discarded here: [discard_es.txt](https://github.com/ideati/challenges/blob/master/Data/Words/discard_es.txt).
- The program must receive two parameters: the book as a text file and the list of discarded words as given here.
- Discard also numeric entities or words mixed with numbers.
- In order to participate, please do a pull request to this repository. We will test it in a headless RPi 3 connected via ssh and working exclusively for the contest. We'll take the best time of five succesive runs.
- There is a penalty of 1 ms for each kb needed to execute the entry. This put interpreted languages at disadvantage. For instance: a shell script will carry the size of the minimal shell needed to run the script.

## Results
The current performance of the reference implementation in a Raspberry Pi 3 Model B Rev 1.2 is:
```sh
$ ./wordc
Word counter v.0.0.1
Use: ./wordc filename.txt [exclusions.txt]

$ time ./wordc pg2000.txt ../discard_es.txt
0.  "no" 6345
1.  "se" 4690
2.  "su" 3352
3.  "don" 2652
4.  "me" 2345
5.  "quijote" 2180
6.  "sancho" 2148
7.  "es" 2142
8.  "yo" 2077
9.  "más" 2044

real    0m0,220s
user    0m0,486s
sys     0m0,020s

$ ls -Al wordc
-rwxr-xr-x 1 jorge jorge 20296 abr 12 03:31 wordc
```
The penalty is: 20.3 kb -> 0.020s.

Time spent by the system is 0.020s.

Total performance for the reference implementation: 0.220 - 0.020 + 0.020 = 0.220 seconds (This is the mark to beat to win the [prize](https://github.com/ideati/challenges/blob/master/PRIZE.md))

Note that the user time is greater than the real time. This happens when a program is making use of parallel execution; there are 4 cores in the Raspberri Pi. The actual elapsed time, as if taken by a stopwatch, is the one labeled "real".
