---
title: "The Christoffel Tree"
date: 2026-11-07T00:00:00Z
draft: false
math: true
---

In our previous post we extended the Stern-Brocot tree to represent turn orders. It turns out this has a name: the [Christoffel tree](https://arxiv.org/abs/2507.15313).

The result of this means there is a rigorous method to generate a balanced turn order that gives the desired ratio of turns between two players.

I'll highlight a few of the learnings from this paper here.

### Christoffel tree

Section 3.2 introduces the Christoffel tree. The construction matches what we discovered in a previous post.

![Christoffel tree](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7j6m12RmDVjxN9o1sUSxfmtYNd4gylv5-cyRnKALDTQ&s#center)

Furthermore, this paper makes visually explicit the connection to the [Bresenham line algorithm](https://en.wikipedia.org/wiki/Bresenham%27s_line_algorithm), though it doesn't reference this by name.

### Periodicity

Section 6.5 concerns periodicity of Christoffel words. They give a method to create a Christoffel word from any two relatively prime integers. I thought this example in particular was well illustrated.

> **Example 1.** Let $p = 4$ and $q = 7$. Then $p$ and $q$ are relatively prime,
> $$
P = \{4, 8, 12, 16, 20, 24\} \quad\text{and}\quad Q = \{7, 14, 21\}.
$$
> The superposition of $P$ and $Q$ is given below, with the elements of $Q$ in boldface.
>
> $$
\begin{array}{ccccccccc}
4 & \mathbf{7} & 8 & 12 & \mathbf{14} & 16 & 20 & \mathbf{21} & 24 \\
x & y & x & x & y & x & x & y & x
\end{array}
$$
>
> Adding the letter $x$ at the start and the letter $y$ at the end, we obtain the
> Christoffel word $xxyxxyxxyxy$ of slope $\tfrac{4}{7}$.

### Stern-Brocot tree

Section 7.3 finally connects the dots directly back to the Stern-Brocot tree.

> The Christoffel tree is isomorphic to the Stern–Brocot tree via the map that associates to a vertex $(u, v)$ of the Christoffel tree the fraction
> $$\dfrac{|uv|_y}{|uv|_x}$$
