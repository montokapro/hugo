---
title: "Three-player Hackenbush Played on Strings"
date: 2026-11-08T00:00:00Z
draft: false
math: true
---

There is a particular diagram from Alessandro Cincotti's paper [*three-player Hackenbush played on strings is $NP$-complete*](https://www.iaeng.org/publication/IMECS2008/IMECS2008_pp226-230.pdf) that is of interest to me, specifically figure 3. I'll write out the Hackenbush strings below. Consider the left margin the floor.

```
01

02

11

22
```

This is considered a *queer* game, because no player can make a move that results in a winning strategy. The only option is to decide which of the other players should win. Now, one could define a hierachical evaluation of position, that determines who should win if no coalition exists. But the stance of J. G. Propp to only consider games with clear winning strategies is very compelling.

I would like to explore n-player games - exploring them could help us extend surreals to the complex number system. Doing this would be quite involved, and require an unusual evaluation heuristic. For the moment, I'll stick to evaluating two player games!