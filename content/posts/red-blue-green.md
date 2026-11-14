---
title: "Red-Blue-Green Hackenbush"
date: 2026-11-13T00:00:00Z
draft: false
math: true
---

I've been taking another look at the graphic here.

![Games born by day 2](https://media.springernature.com/lw1200/springer-static/image/art%3A10.1007%2Fs00182-020-00715-3/MediaObjects/182_2020_715_Fig4_HTML.png#center)

I realize now that I can enumerate a hackenbush tree by continually adding branches to any of the nodes in the tree. Each time a branch is added, it adds a node - a fresh address - to which I can add additional branches. The color of said branches can be whatever I like.

In a single day we can reach something like the following:
$$
\begin{align}
\{ \mid 0 \}_{u,v} &= -u \\
\{ 0 \mid 0 \}_{u,v} &= \ast_1 \\
\{ 0 \mid \}_{u,v} &= v
\end{align}
$$

Note that there are $u + v$ confused values given relative primes $u$ and $v$, where $\ast_0 = 0$ and $\ast_n = \ast_{n \bmod (u + v)}$. This is because a round has $u + v$ total turns.

I am a bit unsure about $\\{ 0 \mid 0 \\}_{u,v} = \ast_1$ specifically. Perhaps a more accurate construction would be one that weights the value between $u$ and $v$ differently.

$$
\{ 0 \mid 0 \}_{u,v} = (v - u)\ast_1
$$

Of course for traditional surreals, this would still reduce to a familiar form.

## A full round

After a full round of days we get to a state that _should_ represent $0$, because a full round of individual green stalks is zero. But this doesn't reduce to zero unless $u = v$, which is a bit concerning. This could be a sign that my construction is incorrect.

$$
\{ u + v - 1 \mid u + v - 1 \}_{u,v} = (u + v)(v - u) = (v^2 - u^2)
$$

Or, it could be a clarification that, given $\\{ \ast_n \mid \ast_n \\}\_{u,v} = \ast_{n+1}$:

$$
\{ u + v - 1 \mid u + v - 1 \}_{u,v} \ne \{ \ast_{u + v - 1} \mid \ast_{u + v - 1} \}_{u,v}
$$
