---
title: "Rotational Stability"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-07-13"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/91685028535/rotational-stability)"
# weight: 1
aliases: ["/posts/20140713-rotational-stability"] # alias url / permalink

tags: ["physics", "math", "visualization"]
categories: ["physics"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
     image: "/images/rotational-stability-intermediate.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---

<!-- create a table for side by side images -->
 |
--- | ---
![](/images/rotational-stability-major.gif) | ![](/images/rotational-stability-minor.gif)


Time for an experiment! Find a book and secure it shut using tape or a rubber band. Now experiment with spinning the book while tossing it into the air. You’ll notice that when the book is spun about its longest or shortest axis it rotates stably, but when spun about its intermediate-length axis it quickly wobbles out of control.

Every rigid body has three special, or [principal axes](http://en.wikipedia.org/wiki/Polhode#Description) about which it can rotate. For a rectangular prism — like the book in our experiment — the principal axes run parallel to the shortest, intermediate-length, and longest edges, each going through the prism’s [center of mass](http://en.wikipedia.org/wiki/Center_of_mass). These axes have the highest, intermediate, and lowest [moments of inertia](http://en.wikipedia.org/wiki/Moment_of_inertia), respectively.

When the book is tossed into the air and spun, either about its shortest or longest principal axis, it continues to rotate about that axis forever (or until it hits the floor). For these axes, this indefinite, stable rotation occurs even when the axis of rotation is slightly perturbed.

When spun about its intermediate principal axis, though, the book also continues to rotate about that axis indefinitely, but only if the axis of rotation is _exactly_ in the same direction as the intermediate principal axis. In this case, even the slightest perturbation causes the book to wobble out of control.

The first simulation above shows a rotation about the unstable intermediate axis, where a slight perturbation causes the book to wobble out of control. The second and third simulations show rotations about the two stable axes.

Unfortunately, as far as my understanding goes, there's no intuitive, non-mathematical explanation as to why rotations about the intermediate principal axis are unstable. If you're interested, you can find the stability analysis [here](http://physics.stackexchange.com/questions/67957/stability-of-rotation-of-a-rectangular-prism).

---

[Mathematica](http://www.wolfram.com/mathematica/) code posted [here](https://gist.github.com/BrianWeinstein/6a8a852c46053c0c8d7d).

Additional sources not linked above: [[1](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.111.1838)] [[2](http://youtu.be/GgVpOorcKqc)] [[3](http://physicscentral.com/experiment/askaphysicist/physics-answer.cfm?uid=20080506030339)] [[4](http://youtu.be/4dqCQqI-Gis)]
