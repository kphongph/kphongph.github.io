---
layout: post
title: Introduction to Sets
---

## Basic Terminology

A **set** is a collection of objects where the **order** and **frequency**
of an object in the collection does not have the meaning. 
A set is said to **contain** its elements.

### Notation

- If $x$ is a member or elements of the set $S$, we write $x \in S$.
- If $x$ is not an element of $S$, we write $x \notin S$.

*Definition 1*: The *empty* set, denoted as $\emptyset$ or $\\{\\}$, 
is the set with no members.

### Set Representation

Sets can be written in a variety ways. In this lecture, there are two
forms for representing the set:

- **Roster** (Tabular) : list the elements if there are only a few
- **Set Builder** (Rule) : specify the sets using predicate to indicate
the attributes of the elements of the set.  

For example, *the set $A$ of all even number less than ten and greater 
than zero* can be representing as

- Roster form as : $A = \\{2, 4, 6, 8\\}$
- Set builder form as : $A = \\{x | x~\mbox{mod}~2 = 0~and~0 \le x < 10\\}$
  - two parts : (1) variable **$x$** reprensenting member of set and 
    (2) **boolean existing condition** of the variable where 
    "|" is read as "such that"

### Common Universal Sets

The following notation is commonly used in general.

- $\mathbb{R}$ is the set of real numbers,
- $\mathbb{N}$ is the set of natural numbers (i.e., $\\{0, 1, 2, 3, \ldots\\}$)
- $\mathbb{Z}$ is the set of integers (i.e., 
  $\\{\ldots, -2, -1, 0, 1, 2, \ldots\\}$)
- $\mathbb{Z^+}$ is the set of positive integers 
  (i.e., $\\{1, 2, 3, \ldots\\}$

### Complements and Subsets

*Definition 2*: The **complement** of set $A$ can be denoted as $\bar{A}$ 
which representing a set $\\{x | x \notin A \\}$.

*Definition 3*: A set $A$ is a **subset** of a set $B$, denoted as 
$A \subseteq B$, if and only if, every element of $A$ is also an elements of 
$B$ 

*Definition 4*: A set $A$ is a **proper subset** of a set $B$, denoted as 
$A \subset B$, if and only if, every element of $A$ is also an elements of 
$B$ but $A \neq B$.

> Example 1: Elements and Subsets
>
> Given a set $S = \\{1, 2, \\{1\\}, \\{3\\}\\}$, then 
>
> - $ 2 \in S$

