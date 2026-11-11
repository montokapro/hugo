---
title: "Exploring Turn Orders via the Stern-Brocot Tree"
date: 2026-11-04T00:00:00Z
draft: false
math: true
---

We've covered the Stern-Brocot matrix representation previously. Succinctly, we can describe it with iterations of $Left$ and $Right$ functions on the identity matrix.

$$
I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
\quad
M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$

$$Left(M) = M \cdot L = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} a+b & b \\ c+d & d \end{pmatrix}$$

$$Right(M) = M \cdot R = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}$$

What would happen if we took the Stern-Brocot tree and replaced the mediant operator with a concatenation? Instead of the identity matrix, we'll start with two players $1$ and $0$ taking alternate turns. We'll adjust the turn orders with left and right functions that concatenate turn structures together.

$$
I = \begin{pmatrix} 0 & 1 \end{pmatrix}
\quad
M = \begin{pmatrix} a & b \end{pmatrix}
$$

$$Left(M) = \begin{pmatrix} a & a || b \end{pmatrix}$$

$$Right(M) = \begin{pmatrix} a || b & b \end{pmatrix}$$

In standard play under combinatory game theory, taking a turn is a disadvantage. Now, say you want to give player $0$ an advantage. You can add an extra turn for player $1$ so that there are two turns for every player $0$ turn.

$$
\footnotesize
\begin{matrix}
0 \mid 1 \\
{
\begin{matrix}
\swarrow && \searrow \\
0 \mid \textcolor{#0000FF}{0}1 && 0\textcolor{#FF0000}{1} \mid 1 \\
{
  \begin{matrix}
  \swarrow && \searrow \\
  0 \mid \textcolor{#0000FF}{0}01 && 0\textcolor{#FF0000}{01} \mid 01 \\
  {
    \begin{matrix}
    \swarrow && \searrow \\
    0 \mid \textcolor{#0000FF}{0}001 && 0\textcolor{#FF0000}{001} \mid 001
    \end{matrix}
  } && {
    \begin{matrix}
    \swarrow && \searrow \\
    001 \mid \textcolor{#0000FF}{001}01 && 001 \mid \textcolor{#FF0000}{001}01
    \end{matrix}
  }
  \end{matrix} 
} && {
  \begin{matrix}
  \swarrow && \searrow \\
  01 \mid \textcolor{#0000FF}{01}1 && 01\textcolor{#FF0000}{1} \mid 1 \\
  {
    \begin{matrix}
    \swarrow && \searrow \\
    01 \mid \textcolor{#0000FF}{01}011 && 01\textcolor{#FF0000}{011} \mid 011
    \end{matrix}
  } && {
    \begin{matrix}
    \swarrow && \searrow \\
    011 \mid \textcolor{#0000FF}{011}1 && 011\textcolor{#FF0000}{1} \mid 1
    \end{matrix}
  }
  \end{matrix}
}
\end{matrix}
}
\end{matrix}
$$

To give player $0$ an advantage, preppend the left partition of the round onto the right partition. To give player $1$ an advantage, append the right partition of the round onto the left partion.

Why does it matter whether we prepend or append? Why does the order rather than the ratio of turns matter at all? By constructing turn order in this fashion we seem to always generate a balanced cyclic sequence. We don't frontload turns for any one player, giving us an even turn distribution. For some games this can be incredibly important - imagine if you let your niece play three turns of tic-tac-toe in a row before you went once!

Instead, using this tree we can hone in on the perfect tic-tac-toe experience. The tree is totally ordered from left to right, with maximum advantage for player $1$ on the left and maximum advantage for player $0$ on the right. Each time you adjust your spot on the tree, you are refining the handicap that equalizes two players skill levels. This does hinge on some impractical assumptions, but for an imbalanced game, with open information, under perfect play, for an alternating turn structure, we could balance the game precisely. This may seem like an absurd number of conditions, but they are the same conditions that define the games of the surreal numbers.
