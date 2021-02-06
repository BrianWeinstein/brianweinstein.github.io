---
title: "Three-Body Problem in 3D"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-05-12"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/85569734683/three-body-problem-in-3d)"
# weight: 1
aliases: ["/posts/20140512-three-body-problem-3d"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
    image: "/images/three-body-problem-3d.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---


A couple of weeks ago I made a [post](http://fouriestseries.tumblr.com/post/83838450432/planar-three-body-problem) about the **[classical three-body problem](http://en.wikipedia.org/wiki/Three-body_problem)**, which involves determining the motion of three masses interacting via [gravity](http://en.wikipedia.org/wiki/Newton) over time.

In that simulation, the three masses were restricted to a plane. Even though we live in [three spatial dimensions](http://en.wikipedia.org/wiki/Dimension_(mathematics_and_physics)#Spatial_dimensions), a two-dimensional model for celestial orbits isn’t such a bad approximation – the orbits of masses in celestial system are often [within a few degrees](http://www.ast.cam.ac.uk/public/ask/3088) of the same plane.

In the simulation above I’ve built in a third spatial dimension and modeled a system in which the masses _do not_ stay within the same plane. In this simulation, the green and red bodies are 9 and 13 times more massive than the blue body, respectively.

---

The [Mathematica](http://www.wolfram.com/mathematica/) code for this one was a bit long, so I've posted it [here](https://gist.github.com/BrianWeinstein/81df3f7c9a2d7d1d6d9e).
