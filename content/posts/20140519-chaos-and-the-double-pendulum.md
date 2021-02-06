---
title: "Chaos and the Double Pendulum"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-05-19"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/86253333743/chaos-and-the-double-pendulum)"
# weight: 1
aliases: ["/posts/20140519-chaos-and-the-double-pendulum"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
     image: "/images/chaos-double-pendulum.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---


A [chaotic system](http://en.wikipedia.org/wiki/Chaos_theory) is one in which infinitesimal differences in the starting conditions lead to drastically different results as the system evolves.

Summarized by mathematician [Edward Lorenz](http://en.wikipedia.org/wiki/Edward_Lorenz), "Chaos [is] when the present determines the future, but the approximate present does not approximately determine the future."

There's an important distinction to make between a _chaotic_ system and a _[random](http://en.wikipedia.org/wiki/Randomness)_ system. Given the starting conditions, a chaotic system is entirely [deterministic](http://en.wikipedia.org/wiki/Deterministic_system). A random system, on the other hand, is entirely non-deterministic, even when the starting conditions are known. That is, with enough information, the evolution of a chaotic system is entirely predictable, but in a random system there's no amount of information that would be enough to predict the system's evolution.

The simulations above show two slightly different initial conditions for a [double pendulum](http://en.wikipedia.org/wiki/Double_pendulum) — an example of a chaotic system. In the left animation both pendulums begin horizontally, and in the right animation the red pendulum begins horizontally and the blue is rotated by 0.1 radians (≈ 5.73°) above the positive x-axis. In both simulations, all of the pendulums begin from rest.

For more information on how to solve for the motion of a double pendulum, check out my video [here](https://www.youtube.com/watch?v=u2c2VgIg6Bg).



---

[Mathematica](http://www.wolfram.com/mathematica/) code posted [here](https://gist.github.com/BrianWeinstein/b7317c5e4f56a9a12cdb).
