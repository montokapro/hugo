---
title: "Hackenbush Conjecture for Strings"
date: 2026-11-11T00:00:00Z
draft: false
math: true
---

Today I present a conjecture. I believe it holds for traditional blue-red Hackenbush, but I still need to find a proof in the literature. It should extend to Hackenbush with Christoffel turn orders, such as $011$.

## Blue-red signs

**Conjecture 1.** All Hackenbush trees beginning with a blue stalk are positive, regardless of the number of turns each player takes in a round.

**Conjecture 2.** All Hackenbush trees beginning with a red stalk are negative, regardless of the number of turns each player takes in a round.

I believe this should hold because we are using an arithmetic mean, which bounds the results. The bounds should be the same even if the mean is weighted.

## Induction on strings

**Conjecture 3.** Hackenbush strings are ordered like trie paths. That is, for bit strings $X$, $Y$ and $Z$,
$$
X0Y \;<\; X \;<\; X1Z,
$$

For example, given a Hackenbush string such as $s_{brrb}$, we can quickly eliminate options when evaluating, without needing to know the exact Christoffel word. Let $u$ be the number of blue turns in a round and $v$ the number of red turns in a round. Then
$$
\begin{aligned}
s_{\text{brrb}} &= u \cdot \max(s_{\text{ground}}, s_{\text{brr}}) + v \cdot \min(s_{b}, s_{\text{br}}) \\
&= u \cdot s_{\text{brr}} + v \cdot s_{\text{br}}.
\end{aligned}
$$