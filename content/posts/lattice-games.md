---
title: "On the Lattice Structure of Finite Games"
date: 2026-11-05T00:00:00Z
draft: true
math: true
---

Today I'd like to take a look at the paper [On the lattice structure of finite games](https://www.researchgate.net/publication/228573794_On_the_lattice_structure_of_finite_games). This paper proves that "games born by day n form a distributive lattice".

## What is a lattice?

Intuitively, I think of a lattice through the lens of a hasse diagram.

[Hasse diagram](https://thumb.wikimedia.org/wikipedia/commons/thumb/9/9b/Hypercubeorder_binary.svg/960px-Hypercubeorder_binary.svg.png?utm_source=en.wikipedia.org&utm_campaign=imageinfo&utm_content=thumbnail)

If you start at the middle row of this graph, you can see that going up in this graph uses a bitwise or between two elements, and going down uses a bitwise and. These are the join and meet operations of the lattice, respectively. Going up amounts to taking the maximum of two elements, and going down amounts to taking the minimum. This particular lattice is also bounded, such that $0000$ is the minimum of all elements and $1111$ is the maximum of all elements. Boolean logic is distributive, so this lattice is distributive too.

## Games born by day n

When this paper describes "games born by day n" they are refering to the surreal, but not exclusively the surreal numbers. Each time you add a possible move that a player could take, you create a more complicated game (assuming that those moves don't actually simplify how the game plays out by providing short cuts).

The surreals are often represented by the game of Hackenbush. Games of red-blue Hackenbush describe the surreal *numbers*, but to expand to the more general surreal *games* we need to add green branches that can be removed by either player. A Hackenbush game made of only these green branches is isomorphic to the game of Nim. Studying Nim and red-blue-green Hackenbush opens us up to the concept of **nimbers** where numbers can be confused with each other, and the ordering is dependent on the player order of the games. For example $*$ is confused with $0$ and $1*$ is confused with the number $1$.

## A visual representation

This graphic was what attracted me to this paper.

[Games born by day 2](https://media.springernature.com/lw1200/springer-static/image/art%3A10.1007%2Fs00182-020-00715-3/MediaObjects/182_2020_715_Fig4_HTML.png)

Specifically, these graphics show me how one can perturb games to form other interesting games. It shows us how to merge two games that are not adjacent on the surreal number tree to form a new game!