---
layout: post
title: Lecture Note (01/21/2015)
---
## Advanced Analysis of Algorithm  
### Last Lecture  

1. Dynamic Programming  
  -  Assembly-line scheduling
  -  Matrix-chain multiplication   

### Today

1. Dynamic Programming
  - Shortest Path Problem
  - Longest Common Subsequence
2. Greedy Algorithms
  - Activity-selection problem
  - Knapsack problem (both 0-1 and fractional)  
  - **Matroids**
  - Task-scheduling problem  
  - Coin changing problem  

## Lecture 
Dynamic Programming = Smart Exhaustive  
- Optimal substructure  
- Overlapping subproblems  
- Memoization  

##Shortest Path Problem

Find the minimum summation of weighted edge of given vertex $x$ and $y$

##Longest Common Subsequence

$X = \langle A, B, C, B, D, A, B \rangle $  
$Y = \langle B, D, C, A, B, A \rangle $

$c[7, 6] = max \{ c[6, 6], c[7, 5] \}  $
$ c[6, 6] = c[5, 5] + 1  $
$ c[7, 5] = c[6, 4] + 1 $
$ c[5, 5] = max \{ c[5, 4], c[4, 5] \} $  
$ c[6, 4] = c[5, 3] + 1$  
$ c[5, 4] = max \{ c[5, 3], c[4, 4] \}$  
$ c[4, 5] = c[3, 4] + 1$  
$ c[5, 3] = max \{ c[4, 3], c[5, 2] \}$  
...

$c[7, 6] = max \{ c[6, 6], c[7, 5] \}  $
$c[7, 5] =  c[6, 4] + 1$
...
$c[2, 2] = max \{ c[2, 1], c[1, 2] \}$  
$c[2, 1] = c[1,0] + 1$  
$c[1, 2] = max \{ c[0, 2], c[1, 1] \}$    
$c[1, 1] = 0$  

> Written with [StackEdit](https://stackedit.io/).