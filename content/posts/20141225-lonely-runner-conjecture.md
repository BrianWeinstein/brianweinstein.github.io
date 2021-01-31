---
title: "Lonely Runner Conjecture"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-12-25"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/106167251583/lonely-runner-conjecture)"
# weight: 1
aliases: ["/posts/20141225-lonely-runner-conjecture"] # alias url / permalink

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
![](/images/lonely-runner-3.gif) | ![](/images/lonely-runner-4.gif)
![](/images/lonely-runner-5.gif) | ![](/images/lonely-runner-6.gif)
![](/images/lonely-runner-7.gif) | ![](/images/lonely-runner-8.gif)


Imagine _n_ runners on a circular track of length 1. The runners start from the same spot at the same time, and each has a [distinct](http://en.wikipedia.org/wiki/Distinct), [constant](http://en.wikipedia.org/wiki/Constant_(mathematics)) speed. A runner is considered “lonely” whenever it is a distance of at least 1/_n_ from every other runner. The **[Lonely Runner Conjecture](http://en.wikipedia.org/wiki/Lonely_runner_conjecture)** (LRC) states that each runner will eventually, at some point in time, be lonely.

Said differently, the LRC states that for each runner, the spacing around it will eventually be greater than or equal to the spacing it would experience if the all of the runners were equally distributed around the track.

The [conjecture](http://en.wikipedia.org/wiki/Conjecture) has been proven to be true for 7 or fewer runners, but, interestingly enough, has never been proven to work for all cases of 8 or more runners. [In my 8-runner simulation above, I’ve only shown that it works for a specific set of runner speeds — I haven’t proven that it works for _all_ sets of speeds.]

In the GIFs above, an arc appears around a runner whenever the runner is lonely, and the color of a runner fades after it’s been lonely at least once.

---

[Mathematica](http://www.wolfram.com/mathematica/) code posted [here](https://gist.github.com/BrianWeinstein/cf875cdf57c7c6a0c282).

Additional sources not linked above: [[1](http://arxiv.org/abs/0710.4495)] [[2](http://rjlipton.wordpress.com/2012/01/28/the-lonely-runner-conjecture/)] [[3](http://stathletics.tumblr.com/post/21662762724/the-lonely-runner-conjecture)]
