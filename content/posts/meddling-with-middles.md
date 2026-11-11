---
title: "Meddling with Middles"
date: 2026-11-03T00:00:00Z
draft: false
math: true
---

I've already talked about the surreal number tree and Stern-Brocot tree. Both of these are *totally ordered binary trees*. Today I intend to explain why, and show you how to create your own totally order trees.

To build one of these trees, we need to define a **middle function**, $m(l, r)$, that takes a left ancestor $l$ and a right ancestor $r$ and generates an intermediate node. The middle function must satisfy the property:

$$
l < m(l, r) < r
$$

Given two inequal parents at the root of your tree, the strict total order follows naturally:

* When you descend to the **left**, you generate a strictly lesser element.
* When you descend to the **right**, you generate a strictly greater element.
* When you switch directions while descending, you generate an element between the previous two elements.

## Arithmetic Mean

The **arithmetic mean** is the most intuitive middle function:

$$m(l, r) = \frac{l + r}{2}$$

The surreal numbers can be viewed as being built on top of this function, seeded by $-\infty$ and $+\infty$ elements at the root of the tree.

$$m(-\infty, +\infty) = 0, \quad m(-\infty, r) = r - 1, \quad m(l, +\infty) = l + 1, \quad m(l, r) = \frac{l + r}{2}$$

Repeated application of the arithmetic mean generates the **dyadic rationals** — fractions whose denominators are powers of 2 (e.g., $\frac{1}{2}, \frac{3}{4}, -\frac{5}{8}$).

## Mediant

An alternate middle function is the **mediant**:

$$m\left(\frac{a}{b}, \frac{c}{d}\right) = \frac{a + c}{b + d}$$

While the arithmetic mean generates the surreal numbers, the mediant generates the Stern-Brocot tree.

To verify that this fits our requirement, we can look at the mediant inequality. If $\frac{a}{b} < \frac{c}{d}$, then:

$$\frac{a}{b} < \frac{a + c}{b + d} < \frac{c}{d}$$

If we seed with zero and positive infinity (represented by $\frac{0}{1}$ and $\frac{1}{0}$) we get all positive rationals.

## Other middles

There are plenty of other middles that can form interesting and useful trees. There are weighted means, geometric means, harmonic means and more. Anything that satisfies the foundational inequality will do!

