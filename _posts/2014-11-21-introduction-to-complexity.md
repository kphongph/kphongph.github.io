---
layout: post
title: Introduction to Complexity
---

In computer science, we define the **computational problem** as a mapping or relation from *input* to desire *output*. For example, consider the following computation problem as *finding the shortest path between two vertices in the given graph*, the **input** is a graph $G(V, E)$ with two vertices $v\_1 \in V$ and $v\_2 \in V$ and the **output** is an path $p \subseteq E$ from $v\_1$ to $v\_2$ such that $|p|$ is minimum.  

To solve the computation problem, we design the **algorithm**, which is sequence of instructions. For example, as the previous computation problem,  the algorithm is breath-first-search starting from $v\_1$ until we found $v\_2$.

**Computational complexity** is a branch of theory of computation that focuses on understanding the inherent difficulty of computational problems. Given a computational problem, in term of computational complexity, we want to (1) find the **effective method** (e.g., algorithm) $alg\_1$ to solve the problem and (2) able prove that there does not exist a more efficent algorithm than $alg\_1$.

A method is called **effective** for a class of problems if and only if: 
 
- contains finite set of instructions
- finish in finite steps
- produces a correct answer

To study the effective method, we need the mathematical models to represent the method and use those model to analyze its effectiveness. Some examples of models include (1) Turing machines, (2) finite state machines, (3) recursive functions, (4) lambda calculus, (5) combinatory logic, and (6) abstract rewriting systems.


> Written with [StackEdit](https://stackedit.io/).