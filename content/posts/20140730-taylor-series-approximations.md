---
title: "Taylor Series Approximations"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-07-30"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/93348339129/taylor-series-approximations)"
# weight: 1
aliases: ["/posts/20140730-taylor-series-approximations"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
     image: "/images/taylor-series.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false

---

A [Taylor series](http://en.wikipedia.org/wiki/Taylor_series) is a way to represent a function in terms of [polynomials](http://en.wikipedia.org/wiki/Polynomial). Since polynomials are usually much easier to work with than complicated functions, Taylor series have [numerous applications](http://math.stackexchange.com/questions/218421/what-are-the-practical-applications-of-the-taylor-series) in both math and physics.

There are many equations in physics — like the one describing the motion of a [pendulum](http://en.wikipedia.org/wiki/Pendulum_(mathematics)) — that are _impossible_ to solve in terms of [elementary functions](http://mathworld.wolfram.com/ElementaryFunction.html). "Approximations using the first few terms of a Taylor series can make [these] otherwise unsolvable problems" solvable for a restricted [area of interest](http://en.wikipedia.org/wiki/Radius_of_convergence) [[1](http://en.wikipedia.org/wiki/Taylor_series#Analytic_functions)].

The GIF above shows the five-term Taylor series approximation of a sine wave about _x_=0.

---

[Mathematica](http://www.wolfram.com/mathematica/) code:
```
f[x_] := Sin[x]
ts[x_, a_, nmax_] :=
    Sum[(Derivative[n][f][a]/n!)*(x - a)^n, {n, 0, nmax}]
Manipulate[Plot[{f[x], ts[x, 0, nmax]}, {x, -2*Pi, 2*Pi},
    PlotRange -&gt; {-1.45, 1.45},
    PlotStyle -&gt; {{Thick, Cyan}, {Thick, Dotted, Yellow}},
    AxesStyle -&gt; LightGray, Background -&gt; Darker[Gray, 0.8]],
    {nmax, 1, 30, 1}]
```
