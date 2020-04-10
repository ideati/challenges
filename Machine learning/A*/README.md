# A*
This search algorithm is at the basis of many applications, specially map navigation and games. It's the finder of the optimal path and it consists in a branch and bound routine plus a list of extended paths plus a consistent heuristic.

The scope of the extended list is to avoid repeating already extended paths.

The consistent heuristic is an estimation of the magnitude that is being optimized and that satisfies the consistency rule:

|H(x,G)-H(y,G)| <= D(x,y) where x and y are two different nodes and G is the goal. H is the heuristic and D is the magnitude

## Objective
Implement the A* algorithm to obtain the shortest path in the graph defined by map.json. The simpler implementation wins.

## License
Each author retains the rights to his/her code, but each entry shall have a OSI approved license in order to be considered for participation.

## Restrictions
- The code must process any graph with the same topology that the one in the example.
- Choose any programming language, library and/or tool.
- The resulting program can be compiled or interpreted.
- The program shall get the json file, process it and produce the shortest path as a list of nodes.
- The entry that obtain the right solution faster than the reference implementation will receive a prize. There is a penalty of 1 ms per each kb needed to execute the entry (binaries + memory allocated at runtime).
