---
title: "Fourier Series"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-04-23"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/83670623611/a-fourier-series-is-a-way-to-expand-a-periodic)"
# weight: 1
aliases: ["/posts/20140423-fourier-series"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

# cover:
#     image: "/images/rotational-stability-intermediate.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---

![](/images/fourier-series-square.gif)

![](/images/fourier-series-sawtooth.gif)


A [Fourier series](http://en.wikipedia.org/wiki/Fourier_series) is a way to expand a periodic function in terms of sines and cosines. The Fourier series is named after [Joseph Fourier](http://en.wikipedia.org/wiki/Jean-Baptiste_Joseph_Fourier), who introduced the series as he solved for a mathematical way to describe [how heat transfers](http://en.wikipedia.org/wiki/Heat_equation) in a metal plate.

The GIFs above show the 8-term Fourier series approximations of the [square wave](http://en.wikipedia.org/wiki/Square_wave) and the [sawtooth wave](http://en.wikipedia.org/wiki/Sawtooth_wave).

---

[Mathematica](http://www.wolfram.com/mathematica/) code:

```
f[t_] := SawtoothWave[t]
T = 1;
nmax = 18;
a0 = (2/T)*Integrate[f[t], {t, -(T/2), T/2}]
anlist = Table[(2/T)*Integrate[f[t]*Cos[(2*Pi*n*t)/T],
     {t, -(T/2), T/2}], {n, 1, nmax}]
bnlist = Table[(2/T)*Integrate[f[t]*Sin[(2*Pi*n*t)/T],
     {t, -(T/2), T/2}], {n, 1, nmax}]
fs[t_, nmax_] := a0/2 + Sum[anlist[[n]]*Cos[(2*Pi*n*t)/T] +
     bnlist[[n]]*Sin[(2*Pi*n*t)/T], {n, 1, nmax}]
Manipulate[Column[{Plot[{f[t], fs[t, nmax0]}, {t, -1, 1},
     PlotRange -> All, AxesLabel -> {"t", "f(t)"},
     PlotStyle -> {{Thick, Black}, {Thick, Red}},
     ImageSize -> 700, AspectRatio -> 1/2.8],
     Row[{"f(t)=", fs[t, nmax0]}]}], {nmax0, 1, nmax, 1}]
```
