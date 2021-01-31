---
title: "Platonic Solids"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2015-01-20"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/108679777878/platonic-solids)"
# weight: 1
aliases: ["/posts/20150120-platonic-solids"] # alias url / permalink

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
![](/images/platonic-solids-04.gif) | ![](/images/platonic-solids-06.gif)
![](/images/platonic-solids-08.gif) | ![](/images/platonic-solids-12.gif)

![](/images/platonic-solids-20.gif)




A [Platonic solid](http://en.wikipedia.org/wiki/Platonic_solid) is a [polyhedron](http://en.wikipedia.org/wiki/Polyhedron)&nbsp;where (1) each face is the [same](http://en.wikipedia.org/wiki/Congruence_(geometry)) [regular polygon](http://en.wikipedia.org/wiki/Regular_polygon), and (2) each [vertex](http://en.wikipedia.org/wiki/Vertex_(geometry)) joins the same number of [faces](http://en.wikipedia.org/wiki/Face_(geometry)).

The Platonic solids are highly&nbsp;[symmetrical](http://en.wikipedia.org/wiki/Platonic_solid#Symmetry), and, in three dimensions, only five such solids can exist: the tetrahedron, cube, octahedron, dodecahedron, and icosahedron.

This was first proven in [Euclid’s Elements](http://en.wikipedia.org/wiki/Euclid%27s_Elements) around 300&nbsp;B.C., and has since been more rigorously proven using the [Euler characteristic](http://en.wikipedia.org/wiki/Euler_characteristic#Polyhedra). The proofs are relatively easy to follow, and if you’re interested you can check them out both [here](http://en.wikipedia.org/wiki/Platonic_solid#Classification) and [here](http://meandering-through-mathematics.blogspot.com/2011/11/why-are-there-exactly-five-platonic.html).

---

[Mathematica](http://www.wolfram.com/mathematica/) code:
```
pSolids={"Tetrahedron","Cube","Octahedron","Dodecahedron","Icosahedron"}
Manipulate[Graphics3D[
 {Opacity[0.8],Rotate[PolyhedronData[pSolids[[n]],"Faces"],th,{0,0,1}],
  Opacity[0],Circumsphere[PolyhedronData[pSolids[[n]],
    "VertexCoordinates"][[1;;4]]]},
 Boxed->False,SphericalRegion->True],{n,1,5,1},{th,0,2\[Pi]}]
 ```
