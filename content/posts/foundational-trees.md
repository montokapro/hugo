---
title: "The Trees at the Root of Mathematics"
date: 2026-11-01T00:00:00Z
draft: false
math: true
---

Recently, I’ve been fascinated by two different tree structures capable of generating numbers.

### Surreals

John Conway's surreal number system evolved in service of combinatorial game theory. It is a much richer system than our traditional number system. It is capable of expressing various infinities, without which led to invention of calculus. If the surreals had been invented earlier we would have had no need for limits.

In finite time it can generate any dyadic rational (numbers of the form $\frac{n}{2^k}$). It supports linear transformations, and after an infinite amount of iterations called "birthdays", generates infinitesmals and even transcendentals. Unfortunately, to the extent I understand today, there is a nagging asymmetry in the rate the rationals approach $\omega$ and $\frac{1}{\omega}$. On the shown diagram it appears that they are reached on the same birthday, and yet, that would seem to imply that $\omega = 2^\omega$.
![Introduction to surreal numbers by M. Kruskal](https://figures.semanticscholar.org/4c61fc616a94f96ad3bfb8745fe0005feeb78aab/14-Figure1-1.png#)

### Stern-brocot

In contrast, the Stern–Brocot tree generates all positive rationals in finite time. Simpler fractions like $\frac{1}{3}$ appear early (day 3), whereas more complex dyadic fractions like $\frac{3}{8}$ take longer. Here, $\omega$ and $\frac{1}{\omega}$ are clearly reached on the same day, because there is a left-right symmetry via the reciprocal.

![By Aaron Rotenberg - Own work, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=4000433](https://thumb.wikimedia.org/wikipedia/commons/thumb/3/37/SternBrocotTree.svg/3840px-SternBrocotTree.svg.png?utm_source=en.wikipedia.org&utm_campaign=imageinfo&utm_content=thumbnail#center)

I find the Stern-Brocot tree a bit more elegant. It produces all positive rationals in finite time. It seems just as capable of generating the transcendentals and exploring infinities and infinitesmals rigorously, though this requires extending the standard tree. 

### Similarities

Both trees, after a countably infinite number of iterations $\omega$, can generate the trancendentals and any missing reals via dedekind-cuts. Both trees are binary, and describe their numbers via a binary path.

I'm interested in extended both of these, and just maybe, stitching the two together to see what numbers are reachable in finite time.

