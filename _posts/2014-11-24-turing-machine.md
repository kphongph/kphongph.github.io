---
layout: post
title: Turing Machines
---

Turing machine is a hypothetical device that manipulates symbols on a strip of tape according to a table of rules. It is easier to prove things about Turning machines because they are so simple and yet they are as powerful as any computers.  

The Turing machine is a finte automaton, which has a single tape of infinite length that can be read from and written to. Each tape cell can hold a finite number of symbols. Tape head implements with a finite control (fixed number of transitions and fixed number of states). Tape can hold finite input string surrounded on either side by an infinite number of blank symbols. If no transition is encoded for a given current state, input symbol, or tape symbol, then the Turing machine dies (i.e., halts).

Turing machine makes a move by considering the three factors: (1) the current state, (2) the current tape contents, and (3) the current head position. A setting of these three items is called a **configuration** of the Turing machine.  For  example, $1011 q\_2 0111$ represents the current sate is $q\_2$, the current tape content is $10110111$, and the current head position is in the second $0$ of the input.

Example, design the turing machine for recognize the language $L = \{ wcw | w \in \{a, b\}^*\}$.

First, we need to outline the description tasks for our machine.
 
 1. *Find* the first unmarked '$a$' or '$b$'
 2. If there is no unmarked '$a$' or '$b$' left in the first '$w$' (i.e., the  first unmarked is '$c$', scan thru the second '$w$' whether it contains either '$a$' or '$b$'. If the second '$w$' does not contain neither '$a$' or '$b$', **accept**. Otherwise **reject**.
 3. *Mark* and *Remember* the first unmarked alphabet in the first '$w$'
 4. *Move* the head until pass alphabet '$c$'
 5. *Check* the first found alphabet in the second '$w$' whether it is same as the alphabet in step 3. If they are not the same, then **reject**.
 6. *Mark* the alphabet in step 5.
 7. *Move* the head to the left-end
 8. *Repeat* to step 1.