---
title: "Signal Collection and Parabolic Reflectors"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-08-11"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/94474567298/signal-collection-and-parabolic-reflectors)"
# weight: 1
aliases: ["/posts/20140811-signal-collection-parabolic-reflectors"] # alias url / permalink

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
![](/images/signal-collection-paraboloid.gif) | ![](/images/signal-collection-sphere.gif)


A [reflector](http://en.wikipedia.org/wiki/Reflector_(antenna)) is a type of antenna that receives and focuses various types of signals. Reflectors have numerous applications, from [satellite dishes](http://en.wikipedia.org/wiki/Satellite_dish) and [telescopes](http://en.wikipedia.org/wiki/Reflecting_telescope), to [long-distance microphones](http://en.wikipedia.org/wiki/Parabolic_microphone) and car headlights. One common feature of these examples is their parabolic shape, giving them the name [parabolic reflectors](http://en.wikipedia.org/wiki/Parabolic_reflector).

It turns out that [paraboloids](http://en.wikipedia.org/wiki/Paraboloid) are the _perfect_ shape for focusing signals from distant sources. When pointed directly at the the incoming signal, a parabolic reflector (GIF 1) collects the signal to a single [focal point](http://en.wikipedia.org/wiki/Focus_(optics)), where a receiver, called a [feed horn](http://electronics.howstuffworks.com/satellite-tv6.htm), is placed to collect the focused transmission.

In many applications, parabolic reflectors are too costly to produce, so [_spherical_ reflectors](http://farside.ph.utexas.edu/teaching/302l/lectures/node136.html) (GIF 2) are used instead. The disadvantage of spherical reflectors is that they have multiple focal points, and therefore produce [blurry results](http://en.wikipedia.org/wiki/Spherical_aberration).

---

[Mathematica](http://www.wolfram.com/mathematica/) code posted [here](https://gist.github.com/BrianWeinstein/be3a2691e37381bdde9b).

This code is incredibly messy and I guarantee there’s a better way to calculate this. Please [contact me](http://fouriestseries.tumblr.com/about) if you have suggestions!
