---
title: "Christoffel Hackenbush"
date: 2026-11-10T00:00:00Z
draft: false
math: true
---

Let's generalize the Hackenbush games from the $01$ and $011$ round structure to Christoffel word turn structures. We use balanced round structures, to get the linearity properties we desire for adding positions together. We don't want our players making tactical decisions, only strategic choices. For this reason, any turn order we consider will be a Christoffel word, reachable from the Christoffel tree. More precisely, at every node is a Christoffel pair, and a Christoffel word is the concatenation of the pair elements. 

![christoffel tree](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7j6m12RmDVjxN9o1sUSxfmtYNd4gylv5-cyRnKALDTQ&s#center)

For example, a valid turn structure would be $00101$.

## Turn ratio

This time, for every $u$ moves player $0$ takes, player $1$ takes $v$ moves. Recall that under standard play, the first player who cannot take a move loses. Therefore, taking a move is a disadvantage.

Again, I represent the floor of Hackenbush as a white circle with a black outline. Player $0$'s edges are blue, and player $1$'s edges are red.

For every move player $0$ takes, player $1$ takes two moves. Recall that under standard play, the first player who cannot take a move loses. Therefore, taking a move is
 a disadvantage.

Here I represent the floor of Hackenbush as a white circle with a black outline.

![balanced](a.svg#center)

$$
u \times \frac{1}{u} + v \times -\frac{1}{v} = 0
$$

We normalize with a magnitude of $1$ such that $u \times s_b = 1$ and $v \times s_r = -1$ It would be certainly possible to normalize differently, like by a factor of $u + v$.

## Rounds

We can again use the weighted arithmetic mean to evaluate hackenbush positions for strings. In groups of $(u + v)$, the best move for both players is to play on independent stalks.

$$
\frac{u \times s_0 + v \times s_1}{u + v}
$$

![blue-red](b.svg#center)

$$
(u + v) \times s_{br} = \frac{1}{u} \quad s_{br} = \frac{1}{u * (u + v)} 
$$

![red-blue](c.svg#center)

$$
(u + v) \times s_{rb} = -\frac{1}{v} \quad s_{rb} = -\frac{1}{v * (u + v)} 
$$

## Larger Hackenbush strings

We can extend this to larger Hackenbush strings again.

$$
(u + v) \times s_{brb} = u \times s_{br} + v \times s_{b}  
$$

$$
(u + v) \times s_{rbr} = u \times s_{r} + v \times s_{rb}  
$$

$$
(u + v) \times s_{brr} = v \times s_{br}  
$$

$$
(u + v) \times s_{rbb} = u \times s_{rb}  
$$

Inductively we get the following, where $s_0$ represents player $0$'s best move and $s_1$ represents player $1$'s best move.  

$$
(u + v) \times s = u \times s_{0} + r \times s_{1} 
$$
