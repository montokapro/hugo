---
title: "The Lattice Structure of n-player Games"
date: 2026-11-06T00:00:00Z
draft: false
math: true
---

Next I am looking at Alessandro Cincotti's paper [*the lattice structure of n-player games*](https://www.researchgate.net/publication/228573794_On_the_lattice_structure_of_finite_games). They prove that "n-player games born by day $d$ form a distributive lattice with respect to every partial order relation $≤ C$, where $C$ is an arbitrary coalition of players."

## Coalitions

Cincotti defines that "A group of players $C$ will form the first coalition, the other players will form the second coalition". I sadly couldn't find a linkable image of the hasse diagram from his paper, but they seem to show that the $\\{0 \mid \mid \\}$ multiplayer game is the inverse of $\\{ \mid 0 \mid 0 \\}$ game. In short, if all players on one team have a move, the inverse would be that all players on the *other* team have a move. This makes intuitive sense as a way of showing the balance of a game under standard play.

## Extending the results

Cincotti's proof is rather general. It applies to, for example, n-player Hackenbush games where each branch is choppable by only a single player. This would be a rather standard construction. It also applies to blue-red Hackenbush games where one team may chop blue branches, and the other team may only chop red branches. These is equivalent to a game with two players but an unequal turn structure. It is this correlation which is especially interesting to me.
