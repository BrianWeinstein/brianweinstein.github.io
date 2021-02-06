---
title: "Gabriel’s Horn and the Painter’s Paradox"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-06-29"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/90296337418/gabriels-horn-and-the-painters-paradox)"
# weight: 1
aliases: ["/posts/20140629-painters-paradox"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
     image: "/images/painters-paradox.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---

[Gabriel’s Horn](http://en.wikipedia.org/wiki/Gabriel) is a three-dimensional horn shape with the counterintuitive property of having a finite volume but an infinite surface area.

This fact results in the [Painter’s Paradox](http://en.wikipedia.org/wiki/Gabriel) — A painter could fill the horn with a finite quantity of paint, “and yet that paint would not be sufficient to coat [the horn’s] inner surface” [[1](http://en.wikipedia.org/wiki/Gabriel)].

If the horn’s bell had, for example, a 6-inch radius, we’d only need about a half gallon of paint to fill the horn all the way up. Even though this half gallon is enough to entirely fill the horn, it’s not enough to even coat a fraction of the inner wall!

The mathematical explanation is a bit confusing if you haven’t taken a first course in calculus, but if you’re interested, you can check it out [here](http://mathworld.wolfram.com/GabrielsHorn.html).

---

[Mathematica](http://www.wolfram.com/mathematica/) code:

```
x[u_, v_] := u
y[u_, v_] := Cos[v]/u
z[u_, v_] := Sin[v]/u
Manipulate[ParametricPlot3D[{{x[u, v], y[u, v], z[u, v]}},
    {u, 1, umax}, {v, 0, 2*Pi},
    PlotRange -&gt; {{0, 20}, {-1, 1}, {-1, 1}},
    Mesh -&gt; {Floor[umax], 20}, Axes -&gt; False, Boxed -&gt; False],
    {{umax, 20}, 1.1, 20}]
```

[Additional source](http://tocontriveandjive.wordpress.com/2014/02/25/gabriels-horn-and-the-painters-paradox/) not linked above.
