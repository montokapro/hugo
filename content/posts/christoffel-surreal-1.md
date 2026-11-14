---
title: "Christoffel Surreals: First Attempt"
date: 2026-11-12T00:00:00Z
draft: false
math: true
---

We are starting to form a sense of how to map numbers to Christoffel Hackenbush games, but mapping numbers to Christoffel surreals remains elusive. Today we take a crack at defining notation for Christoffel surreals.

Each surreal system will be defined by a Christoffel word, which is itself defied by two relatively prime integers $u$ and $v$. We'll use the following notation $\\{ L \mid R \\}_{u,v}$. The tradition surreals are therefore a specialization where $u = 1$ and $v = 1$.

$$
\{ L \mid R \}_{1,1} = \{ L \mid R \}
$$

## Weighted arithmetic mean

Extending the arithmetic mean in *Winning Ways for you Mathematical Plays* looks like:
$$
\{ L \mid R \}_{u,v} = \frac{u \times L + v \times R}{u + v}
$$

This suggests that the following two equalities should hold.

$$
\begin{aligned}
\{ 0 \mid 1 \}_{u,v} = \frac{v}{u + v} \\
\{ -1 \mid 0 \}_{u,v} = \frac{-u}{u + v}
\end{aligned}
$$

## Rediscovering the identities

Part of the elegance of the traditional surreals is that in a single generation we move from the additive identity to the multiplicative identity and multiplicative inverse, helping to define a **ring**.

$$
\{ \mid 0 \} = -1 \quad < \quad \{ \mid \} = 0 \quad < \quad \{ 0 \mid \} = 1
$$

We can preserve this inequality easily, but we lose the multiplicative identities in the process.

$$
\{ \mid 0 \}_{u,v} = -u \quad < \quad \{ \mid \}_{u,v} = 0 \quad < \quad \{ 0 \mid \}_{u,v} = v
$$

Luckily, we know that $-1$, $1$, and all other integers are representable via Bézout's identity with addition because $u$ and $v$ are relatively prime.

## Beyond the dyadics

I'm still trying to figure out how to generalize the formula that generates the dyadics.

$$
\frac{2p + 1}{2^{n+1}} = \{ \frac{2p}{2^{n+1}} \mid \frac{2p + 2}{2^{n+1}} \} = \{ \frac{p}{2^n} \mid \frac{p + 1}{2^n} \}_{u,v}
$$

Likely, the formula will take this shape:
$$
\{ \frac{}{(u + v)^n} \mid \frac{}{(u + v)^n} \}_{u,v}
$$

This is the last piece necessary to define the **simplest form** in *Winning Ways for Mathematical Plays*.

$$
\begin{aligned}
0 &= \{ \mid \}_{u,v} \\
v \times (n + 1) &= \{ v \times n \mid \}_{u,v} \\
u \times (-n - 1) &= \{ \mid u \times -n \}_{u,v} \\
\frac{}{} &= \{ \frac{}{(u + v)^q} \mid \frac{}{(u + v)^q} \}_{u,v}
\end{aligned}
$$