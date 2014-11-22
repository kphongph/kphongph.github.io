---
layout: post
title: Introduction to Complexity
---

In computer science, we define the **computational problem** as a mapping or relation from *input* to desire *output*. For example, consider the following computation problem as *finding the shortest path between two vertices in the given graph*, the **input** is a graph $G(V, E)$ with two vertices $v1 \in V$ and $v_2 \in V$ and the **output** is an path $p \subseteq E$ from $v_1$ to $v_2$ such that $|p|$ is minimum.  

To solve the computation problem, we design the **algorithm**, which is sequence of instructions. For example, as the previous computation problem,  the algorithm is breath-first-search starting from $v_1$ until we found $v_2$.

**Computational complexity** is a branch of theory of computation that focuses on understanding the inherent difficulty of computational problems. Given a computational problem, in term of computational complexity, we want to (1) find the best algorithm $alg_1$ to solve the problem and (2) able prove that there does not exist a more efficent algorithm than $alg_1$.


> Written with [StackEdit](https://stackedit.io/).