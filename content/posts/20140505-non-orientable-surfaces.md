---
title: "Non-Orientable Surfaces"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-05-05"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/84869520663/non-orientable-surfaces)"
# weight: 1
aliases: ["/posts/20140505-non-orientable-surfaces"] # alias url / permalink

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

<!-- create a table for side by side images -->
 |
--- | ---
![](/images/non-orientable-surfaces-klein-bottle.gif) | ![](/images/non-orientable-surfaces-mobius-strip.gif)



An [orientable](http://en.wikipedia.org/wiki/Orientability) surface is a surface on which it’s possible to make a consistent definition of direction. Most surfaces we encounter – like spheres, planes, and tori (doughnut shapes) – are orientable. When visualized in three dimensions, orientable surfaces have two distinct sides.

Non-orientable surfaces, on the other hand, have only one side. From [Wikipedia](http://en.wikipedia.org/wiki/Orientability#Orientable_surfaces), “The essence of one-sidedness is that [an] ant can crawl from one side of the surface to the ‘other’ without going through the surface or flipping over an edge, but simply by crawling far enough.” At any point on a non-orientable surface it’s impossible to uniquely define, for example, the “[clockwise](http://en.wikipedia.org/wiki/Right-hand_rule#Direction_associated_with_a_rotation)” direction.

The GIFs above show two examples of non-orientable surfaces: a [Klein bottle](http://en.wikipedia.org/wiki/Klein_bottle) and a [Möbius strip](http://en.wikipedia.org/wiki/M%C3%B6bius_strip).

---

[Mathematica](http://www.wolfram.com/mathematica/) code [Klein Bottle]:
```
xk[u_, v_] := (-2/15)*Cos[u]*(3*Cos[v] - 30*Sin[u] +
   90*Cos[u]^4*Sin[u] - 60*Cos[u]^6*Sin[u] + 5*Cos[u]*Cos[v]*Sin[u])
yk[u_, v_] := (-15^(-1))*Sin[u]*(3*Cos[v] - 3*Cos[u]^2*Cos[v] -
   48*Cos[u]^4*Cos[v] + 48*Cos[u]^6*Cos[v] - 60*Sin[u] +
   5*Cos[u]*Cos[v]*Sin[u] - 5*Cos[u]^3*Cos[v]*Sin[u] -
   80*Cos[u]^5*Cos[v]*Sin[u] + 80*Cos[u]^7*Cos[v]*Sin[u])
zk[u_, v_] := (2/15)*(3 + 5*Cos[u]*Sin[u])*Sin[v]
kb[u_, v_] := {xk[u, v], yk[u, v], zk[u, v]}
Manipulate[ParametricPlot3D[kb[u, v], {u, 0, umax}, {v, 0, 2*Pi},
   PlotRange -> {{-1.8, 2}, {0, 4.5}, {-0.75, 0.75}}, Axes ->
   False, Boxed -> False, PlotStyle -> {Opacity[0.65]},
   Mesh -> {20, 11}, MeshStyle ->
   Directive[Gray, Opacity[0.65], Thickness[0.003]]],
   {umax, 0.001, Pi}]
```

[Mathematica](http://www.wolfram.com/mathematica/) code [Möbius Strip]:
```
xm[u_, v_] := (1 + (v/2)*Cos[u/2])*Cos[u]
ym[u_, v_] := (1 + (v/2)*Cos[u/2])*Sin[u]
zm[u_, v_] := (v/2)*Sin[u/2]
ms[u_, v_] := {xm[u, v], ym[u, v], zm[u, v]}
Manipulate[ParametricPlot3D[
   ms[u, v], {u, 0, umax}, {v, -1, 1},
   PlotRange -> {{-1.1, 1.5}, {-1.5, 1.5}, {-0.5, 0.5}},
   PlotStyle -> {Opacity[0.65]}, Axes -> False, Boxed ->
   False,  Mesh -> {20, 5}, MeshStyle ->
   Directive[Gray, Opacity[0.65], Thickness[0.003]]],
   {umax, 0.001, 2*Pi}]
```
