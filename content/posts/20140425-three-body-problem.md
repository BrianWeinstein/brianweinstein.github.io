---
title: "Three-Body Problem on a Plane"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-04-25"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/83838450432/planar-three-body-problem)"
# weight: 1
aliases: ["/posts/20140425-three-body-problem"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
     image: "/images/three-body-problem.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---


Given the starting positions, velocities, and masses of three objects interacting via [gravity](http://en.wikipedia.org/wiki/Newton), the [classical three-body problem](http://en.wikipedia.org/wiki/Three-body_problem) involves determining the motions of the three particles throughout time.

What’s cool about the three-body system is that it’s _impossible_ to solve for the motions of the objects exactly. That is, we can’t write down an _equation_ that describes the system. Instead of finding an exact solution, we solve the system [numerically](http://www.myphysicslab.com/numerical_vs_analytic.html), which amounts to finding an accurate approximation.

The three-body problem is an example of a [chaotic system](http://en.wikipedia.org/wiki/Chaos_theory), meaning that even a slight change in the starting conditions _drastically_ changes the time-evolution of the system.

The GIF above shows a planar (i.e., two-dimensional) three-body system.

---

[Mathematica](http://www.wolfram.com/mathematica/) code:

```
G = 1; time = 30;
mA = 1; xA0 = 0; yA0 = 0; vxA0 = 0; vyA0 = 0;
mB = 1; xB0 = 1; yB0 = 0; vxB0 = 0; vyB0 = 0;
mC = 1; xC0 = 0; yC0 = 0.8; vxC0 = 0; vyC0 = 0;
soln1 = NDSolve[
    {mA*Derivative[2][xA][t] ==
     -((G*mA*mB*(xA[t] - xB[t]))/((xA[t] - xB[t])^2 +
      (yA[t] - yB[t])^2)^(3/2)) -
      (G*mA*mC*(xA[t] - xC[t]))/((xA[t] - xC[t])^2 +
      (yA[t] - yC[t])^2)^(3/2),
    mA*Derivative[2][yA][t] ==
      -((G*mA*mB*(yA[t] - yB[t]))/((xA[t] - xB[t])^2 +
      (yA[t] - yB[t])^2)^(3/2)) -
      (G*mA*mC*(yA[t] - yC[t]))/((xA[t] - xC[t])^2 +
      (yA[t] - yC[t])^2)^(3/2),
    mB*Derivative[2][xB][t] ==
      -((G*mB*mC*(xB[t] - xC[t]))/((xB[t] - xC[t])^2 +
      (yB[t] - yC[t])^2)^(3/2)) -
      (G*mB*mA*(xB[t] - xA[t]))/((xB[t] - xA[t])^2 +
      (yB[t] - yA[t])^2)^(3/2),
    mB*Derivative[2][yB][t] ==
      -((G*mB*mC*(yB[t] - yC[t]))/((xB[t] - xC[t])^2 +
      (yB[t] - yC[t])^2)^(3/2)) -
      (G*mB*mA*(yB[t] - yA[t]))/((xB[t] - xA[t])^2 +
      (yB[t] - yA[t])^2)^(3/2),
    mC*Derivative[2][xC][t] ==
      -((G*mC*mA*(xC[t] - xA[t]))/((xC[t] - xA[t])^2 +
      (yC[t] - yA[t])^2)^(3/2)) -
      (G*mC*mB*(xC[t] - xB[t]))/((xC[t] - xB[t])^2 +
      (yC[t] - yB[t])^2)^(3/2),
    mC*Derivative[2][yC][t] ==
      -((G*mC*mA*(yC[t] - yA[t]))/((xC[t] - xA[t])^2 +
      (yC[t] - yA[t])^2)^(3/2)) -
      (G*mC*mB*(yC[t] - yB[t]))/((xC[t] - xB[t])^2 +
      (yC[t] - yB[t])^2)^(3/2),
    xA[0] == xA0, yA[0] == yA0,
    Derivative[1][xA][0] == vxA0, Derivative[1][yA][0] == vyA0,
    xB[0] == xB0, yB[0] == yB0,
    Derivative[1][xB][0] == vxB0, Derivative[1][yB][0] == vyB0,
    xC[0] == xC0, yC[0] == yC0,
    Derivative[1][xC][0] == vxC0, Derivative[1][yC][0] == vyC0
    },
    {xA, yA, xB, yB, xC, yC},{t, 0, time}, MaxSteps -> 100000]
x1[t_] := Evaluate[xA[t] /. soln1[[1,1]]]
y1[t_] := Evaluate[yA[t] /. soln1[[1,2]]]
x2[t_] := Evaluate[xB[t] /. soln1[[1,3]]]
y2[t_] := Evaluate[yB[t] /. soln1[[1,4]]]
x3[t_] := Evaluate[xC[t] /. soln1[[1,5]]]
y3[t_] := Evaluate[yC[t] /. soln1[[1,6]]]
Manipulate[Show[
    {ParametricPlot[
      {{x1[t], y1[t]}, {x2[t], y2[t]}, {x3[t], y3[t]}},
      {t, tmax - 0.5, tmax},
      Axes -> False, PlotRange -> {{-0.55, 1.45},
      {-0.55, 1.08}}, PlotStyle -> {Red, Green, Blue},
      GridLines -> {Table[0.25*x + 0.07, {x, -100, 100}],
      Table[0.25*y + 0.01, {y, -100, 100}]},
      GridLinesStyle -> Directive[LightGray]]},
    {Graphics[{Opacity[0.7], EdgeForm[Directive[Black]], Red,
      Disk[{x1[tmax], y1[tmax]}, 0.03], Green,
      Disk[{x2[tmax], y2[tmax]}, 0.03], Blue,
      Disk[{x3[tmax], y3[tmax]}, 0.03]}]}, ImageSize -> 600],
    {tmax, 6.05, 16.05}]
```
