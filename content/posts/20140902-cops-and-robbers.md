---
title: "Cops and Robbers (and Zombies and Humans)"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-09-02"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/96488907348/cops-and-robbers-and-zombies-and-humans)"
# weight: 1
aliases: ["/posts/20140902-cops-and-robbers"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

# cover:
#     image: "/images/wave-equation-1.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---

<!-- create a table for side by side images -->
 |
--- | ---
![](/images/cops-robbers-1.gif) | ![](/images/cops-robbers-2.gif)


Cops and Robbers is a mathematical game in which pursuers (cops) attempt to capture evaders (robbers). The game is one of many [pursuit-evasion](http://en.wikipedia.org/wiki/Pursuit-evasion) games, each of which is governed by a [different](http://en.wikipedia.org/wiki/Pursuit-evasion#Continuous_formulation) set of rules. The general goal of these problems is to determine the number of pursuers required to capture a given number of evaders.

The GIFs above show two versions of the game. The first is similar to the standard Cops and Robbers rendition, and the second is best described as "Zombies and Humans".

In both versions, an evader moves in the direction that gets it furthest away from the pursuers (focusing more on the closer pursuers), and a pursuer moves in the direction that gets it closest to the evaders (focusing more on the closer evaders).

In the first simulation, members of both groups have a constant speed. In the second simulation, members of a group move more quickly the closer they are to members of the opposite group, and slower when further away.

---

[Mathematica](http://www.wolfram.com/mathematica/) code posted [here](https://gist.github.com/BrianWeinstein/8f563fd69ada934246d9).

Additional sources not linked above: [[1](http://mathematica.stackexchange.com/questions/40375/how-to-make-a-points-position-time-dependent-given-a-formula-for-the-next-step)] [[2](http://math.bard.edu/student/pdfs/tina-zhang.pdf)]
