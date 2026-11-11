---
title: "Imbalanced Turn Order Hackenbush"
date: 2026-11-09T00:00:00Z
draft: false
math: true
---

Today I get to do something fun - analyze Hackenbush games for imbalanced turn orders! I want to start simple, so I'll only consider the specific turn order $011$ for players $0$ and $1$. In any given round, player $0$ will move once and player $1$ will move twice.

## Turn ratio

For every move player $0$ takes, player $1$ takes two moves. Recall that under standard play, the first player who cannot take a move loses. Therefore, taking a move is
 a disadvantage.

Here I represent the floor of Hackenbush as a white circle with a black outline. By convention, player $0$'s edges are blue, and player $1$'s edges are red.

![balanced](imbalanced-turn-order-1-a.svg#center)

$$
1 \times s_b + 2 \times s_r = 0
$$

If we continue to treat player $0$ stalks as having a value of $1$, then player $1$ stalks have a value of $-\frac{1}{2}$. We can place these on a unit circle and the root then becomes the centroid of these stalks.

![unit circle](imbalanced-turn-order-1-b.svg#center)

## Rounds

We can use the weighted arithmetic mean to extend the surreal's method of evaluating hackenbush positions for strings. In groups of three, the best move for both players is to play on independent stalks.

$$
\frac{s_b + 2 \times s_r}{3}
$$

A red-blue stalk is worth $-\frac{1}{6}$

![red-blue stalk](imbalanced-turn-order-1-c.svg#center)

$$
3 \times s_{rb} = -\frac{1}{2} \quad s_{rb} = -\frac{1}{6} 
$$

A blue-red stalk is worth $\frac{2}{3}$

![blue-red stalk](imbalanced-turn-order-1-d.svg#center)

$$
3 \times s_{br} = 2 \times 1 \quad s_{br} = \frac{2}{3}
$$

We can extend this to larger stalks as well.

A red-blue-red stalk is worth $-\frac{5}{18}$

![red-blue-red](imbalanced-turn-order-1-e.svg#center)

$$
3 \times s_{rbr} = 1 \times -\frac{1}{2} + 2 \times -\frac{1}{6} = -\frac{5}{6} \quad s_{rbr} = -\frac{5}{18} 
$$

A blue-red-blue stalk is worth $-\frac{1}{6}$

![blue-red-blue](imbalanced-turn-order-1-f.svg#center)

$$
3 \times s_{br} = 2 \times \frac{2}{3} \quad s_{br} = \frac{4}{3}
$$

## Triadics

Instead of the dyadics, this Hackenbush construction can express all of the triadics in finite time, and a bit more.

$$
\frac{n}{1 \times 2 \times (3 ^ k)} 
$$

For example, $\frac{1}{3} = s_b + 4 \times s_r$.
