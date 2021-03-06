# maze-generator
## Introduction
Generate a random maze represented as a 2D array of ones and zeros using depth-first search. Note that the "symbolic maze" generated is showing the actual path forged by the algorithm; if this were to be drawn as a true maze, the blank spaces and asterisks would be swapped so that blank spaces would represent the potential path and asterisks would represent walls.

## Next steps
* Modify algorithm so that the path charted doesn't form awkward corners where asterisks are diagonal neighbors
* Pick arbirary maze start and finish
* Write complementary code to solve the generated mazes
* Generate three dimensional mazes

## Sample output
```
RAW MAZE
[1, 0, 1, 1, 0, 0, 0, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 0, 1, 0, 1, 1]
[1, 0, 0, 1, 1, 1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 1, 1, 1, 0]
[1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 1, 0, 0, 1, 0, 0, 1, 0, 1, 1, 0, 1, 0, 1, 0]
[0, 1, 0, 1, 1, 1, 0, 1, 1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 1, 0, 0, 1, 0, 1, 1]
[1, 1, 0, 0, 0, 1, 0, 1, 0, 0, 1, 0, 0, 1, 0, 0, 1, 0, 1, 1, 1, 0, 0, 1, 1, 0, 1, 0, 0, 0]
[1, 0, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 0, 1, 0, 0, 1, 0, 0, 0, 1, 1, 1, 0, 1, 0, 1, 1, 1, 0]
[1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 0, 1, 1, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 1]
[1, 1, 1, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 0, 0, 0, 1, 1, 1, 1, 1, 0, 1, 1, 1, 0, 0, 1]
[0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 1, 1, 0, 1]
[1, 1, 0, 1, 0, 1, 0, 1, 0, 1, 1, 1, 1, 1, 0, 0, 0, 1, 0, 1, 1, 1, 1, 0, 1, 0, 0, 1, 0, 1]
[0, 1, 0, 1, 0, 1, 1, 1, 0, 1, 0, 1, 0, 0, 0, 0, 1, 1, 0, 0, 0, 1, 0, 0, 1, 1, 0, 1, 0, 1]
[1, 1, 0, 1, 0, 0, 0, 0, 1, 1, 0, 1, 0, 1, 1, 1, 1, 0, 0, 0, 1, 1, 0, 0, 1, 0, 0, 1, 1, 1]
[1, 0, 0, 1, 0, 0, 1, 1, 1, 0, 0, 1, 1, 1, 0, 0, 0, 0, 1, 1, 1, 0, 1, 1, 1, 0, 0, 0, 1, 0]
[1, 1, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 1, 0, 1, 1, 1, 0]
[0, 1, 0, 1, 0, 1, 0, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 0, 1, 1, 0, 1, 1, 1, 1, 0, 1, 0, 0, 1]
[1, 1, 1, 1, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 1, 0, 0, 1]
[1, 0, 1, 0, 0, 1, 1, 1, 0, 1, 1, 1, 0, 1, 1, 1, 1, 1, 0, 1, 0, 1, 1, 1, 0, 1, 1, 0, 0, 1]
[0, 0, 1, 1, 1, 0, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 1, 0, 0, 1, 0, 0, 1, 1]
[1, 1, 1, 0, 1, 0, 0, 0, 1, 1, 0, 1, 1, 0, 1, 1, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0]
[1, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 1, 1, 1, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 1, 1]
[1, 1, 1, 0, 0, 1, 1, 1, 0, 1, 1, 1, 0, 0, 1, 1, 0, 1, 1, 1, 1, 0, 1, 1, 1, 1, 0, 0, 0, 1]
[1, 0, 1, 0, 0, 1, 0, 1, 0, 0, 0, 1, 0, 1, 0, 1, 1, 0, 0, 0, 0, 1, 1, 0, 0, 1, 0, 1, 1, 1]
[1, 0, 1, 0, 1, 1, 0, 1, 1, 1, 0, 1, 0, 1, 0, 0, 1, 1, 0, 1, 1, 1, 0, 0, 0, 1, 0, 1, 0, 0]
[1, 0, 1, 1, 1, 0, 1, 1, 0, 0, 0, 1, 0, 1, 0, 0, 0, 1, 1, 1, 0, 1, 1, 0, 1, 1, 0, 1, 0, 1]
[1, 0, 0, 0, 0, 0, 1, 0, 1, 1, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 1, 0, 0, 1, 1, 1]
[1, 0, 1, 0, 1, 1, 1, 0, 0, 0, 1, 0, 0, 1, 1, 1, 1, 0, 1, 1, 1, 0, 1, 0, 1, 1, 0, 0, 0, 1]
[1, 1, 1, 0, 1, 0, 1, 1, 0, 1, 1, 0, 0, 1, 0, 0, 1, 1, 1, 0, 1, 1, 0, 0, 0, 1, 1, 1, 0, 1]
[0, 1, 0, 0, 1, 0, 0, 0, 0, 1, 0, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 1, 0, 1, 0, 1, 0, 1]
[1, 1, 1, 0, 1, 1, 0, 1, 1, 1, 0, 1, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 1]
[1, 0, 1, 0, 0, 1, 1, 1, 0, 1, 1, 1, 0, 1, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1]

SYMBOLIC MAZE
*     *  *           *  *  *  *     *  *  *  *  *  *  *     *  *  *  *  *     *     *  *
*        *  *  *  *  *        *  *           *        *        *        *     *  *  *
*  *     *                       *  *  *     *        *        *     *  *     *     *
   *     *  *  *     *  *     *  *     *     *  *     *     *  *     *        *     *  *
*  *           *     *        *        *        *     *  *  *        *  *     *
*     *  *  *  *     *  *  *  *  *     *        *           *  *  *     *     *  *  *
*     *                                *  *     *  *  *                 *           *  *
*  *  *        *  *  *  *  *  *  *  *     *           *  *  *  *  *     *  *  *        *
         *  *  *                          *  *  *  *              *           *  *     *
*  *     *     *     *     *  *  *  *  *           *     *  *  *  *     *        *     *
   *     *     *  *  *     *     *              *  *           *        *  *     *     *
*  *     *              *  *     *     *  *  *  *           *  *        *        *  *  *
*        *        *  *  *        *  *  *              *  *  *     *  *  *           *
*  *     *     *  *                             *  *  *                 *     *  *  *
   *     *     *     *  *  *  *  *  *  *     *  *     *  *     *  *  *  *     *        *
*  *  *  *     *           *           *                 *           *        *        *
*     *        *  *  *     *  *  *     *  *  *  *  *     *     *  *  *     *  *        *
      *  *  *        *  *        *                 *  *  *        *        *        *  *
*  *  *     *           *  *     *  *     *  *              *  *  *  *  *  *  *  *  *
*           *              *        *  *  *        *        *                       *  *
*  *  *        *  *  *     *  *  *        *  *     *  *  *  *     *  *  *  *           *
*     *        *     *           *     *     *  *              *  *        *     *  *  *
*     *     *  *     *  *  *     *     *        *  *     *  *  *           *     *
*     *  *  *     *  *           *     *           *  *  *     *  *     *  *     *     *
*                 *     *  *  *  *     *                          *     *        *  *  *
*     *     *  *  *           *        *  *  *  *     *  *  *     *     *  *           *
*  *  *     *     *  *     *  *        *        *  *  *     *  *           *  *  *     *
   *        *              *     *  *  *  *  *                 *  *  *     *     *     *
*  *  *     *  *     *  *  *     *                 *  *  *           *           *     *
*     *        *  *  *     *  *  *     *  *  *  *  *     *  *  *  *  *  *  *  *  *     *
```
