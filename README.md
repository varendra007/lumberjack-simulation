# lumberjack-simulation

## Problem Description:
You are a lumberjack in a roadside forest. Every day you would like to cut down trees of the maximum value in the limited time that you have. We represent a forest as a rectangular grid of dimensions n by n points. Each edge between the neighboring grid points has a length of 1. At the position of each point, there could be a tree. Each tree is described using the following parameters:

```cpp
height h,
thickness d,
unit weight c,
unit value p.
```
We calculate the value of each tree according to the formula: `p Â· h Â· d`. To cut down the tree, you have to reach it first. You can move only along the edges between the neighboring grid points. To cut down the tree at the position that you occupy you have to select one of four directions (along grid lines) in which the tree will fall. At the beginning of the day, you start in the lower-left corner of the forest, which is located at the point (0,0). You can assume that there is no tree there. If the tree that you cut falls on the other tree, which is lighter than the one that is falling, then this tree will also fall without being cut directly. We say that the tree is heavier if the total weight calculated as c Â· d Â· h is greater than the total weight of the second tree. In this way, one can achieve a domino effect by pushing one tree onto another. We assume that a tree falls on the other when the distance between them is less the height of this tree. Weights of trees do not cumulate - we always take into account only the weight of the tree, which directly fell onto another. If for example tree A falls onto tree B and its weight is greater than weight of tree B then it can push tree B onto another tree C located in the same direction if the distance between B and C is smaller to height of B and, moreover, tree C is lighter than tree B. When comparing trees B and C we do not take into account tree A that lays on tree B. Moreover, if tree B is not lighter than tree A then it blocks tree A and it will not have a chance to fall onto tree C.

Calculate the biggest profit that you can reach during t time units and provide a corresponding sequence of movements. Assume that the walk between the two neighboring grid points takes 1 unit of time, and cutting the tree takes d units of time.

### INPUT
The first line of input contains three integers: 0 < t <= 5,000 representing the time limit for the lumberjack, `0 < n <= 1,000` represending the size of the grid, and `0 < k <= 10,000` denoting the number of trees. In the following k lines there is a description of consequtive trees consisting of six integer numbers `0 <= x, y < n, 0 < h, d <= 20, 0 < c, p <= 500` representing the position of the trees on the grid, their height, thickness, weight and value.

### OUTPUT
On the output specify a list of moves (using move prefix) and cuts (using cut prefix) with the suffix denoting the direction of the action (up, right, down or left), each on a separate line.

### SCORING
For each test case, your program will receive the score equal to the total value of trees that were cut down by the lumberjack. You should maximize this value. For each test with `n <= 25`, your program should execute below 1 second, for `25 < n <= 100`, your program should execute below 10 seconds, and for `n > 100` your program should execute below 60 seconds. For each test the available memory is limited to 1 GB.

### EXAMPLE INPUT
```
11 10 5
2 3 4 5 2 2
2 6 3 1 1 3
2 7 2 2 2 4
5 5 10 3 1 5
4 3 5 5 2 6
```
### EXAMPLE OUTPUT

```
move right
move right
move up
move up
move up
cut up
move right
```
![image](https://github.com/varendra007/lumberjack-simulation/assets/88757164/cab0125e-8418-4d2b-a208-41ba63b40090)

## OVERALL STANDING AND SCORE
![Screenshot from 2023-09-28 14-28-50](https://github.com/varendra007/lumberjack-simulation/assets/88757164/7a0443d1-16c1-4b2b-b10b-a51e08423e66)


