---
title: "Sonic Booms and the Doppler Effect"
# description: "asdf"
# summary: "asdf"
author: "Brian Weinstein"
date: "2014-05-28"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/87143947768/sonic-booms-and-the-doppler-effect)"
# weight: 1
aliases: ["/posts/20140528-sonic-boom-doppler-effect"] # alias url / permalink

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
![](/images/sonic-boom-doppler-effect-1.gif) | ![](/images/sonic-boom-doppler-effect-2.gif)
![](/images/sonic-boom-doppler-effect-3.gif) | ![](/images/sonic-boom-doppler-effect-4.gif)

The [Doppler effect](http://en.wikipedia.org/wiki/Doppler_effect) is the shift in the [frequency](http://en.wikipedia.org/wiki/Frequency) of a wave observed when the source of the [wave](http://en.wikipedia.org/wiki/Wave) (or the [medium](http://en.wikipedia.org/wiki/Transmission_medium) through which the wave travels) is moving relative to the observer.

We’re most familiar with the Doppler effect as it appears in [sound waves](http://en.wikipedia.org/wiki/Sound_wave#Longitudinal_and_transverse_waves) traveling through air (i.e., pressure waves) – think of how the pitch of a siren drops as an emergency vehicle passes you. The first GIF shows a stationary source and the second shows a source moving to the right at 40% the [speed of sound](http://en.wikipedia.org/wiki/Speed_of_sound). Notice in the second GIF how the wavefronts are closer together in front of the source (producing a higher frequency) and further apart behind it (producing a lower frequency).

The Doppler effect is interesting in its own right, but things get much more exciting when the source travels at speeds greater than or equal to the speed of sound.

When the source travels at the speed of sound (GIF 3) the source will always be at the leading edge of the waves it produces, and when traveling faster than the speed of sound (GIF 4), the source will always be in front of the waves it produces. In both of these cases, notice how the waves overlap with each other. The high pressure areas of each wave [constructively interfere](http://en.wikipedia.org/wiki/Interference_(wave_propagation)) and produce a region of extremely high pressure (much higher than in the surrounding areas). This rapid rise in air pressure is a [shock wave](http://en.wikipedia.org/wiki/Shock_wave), and the sound associated with it is a [sonic boom](http://en.wikipedia.org/wiki/Sonic_boom).

In each of the GIFs above we see the radiating wavefronts on the left, and the pressure distribution and interference of the waves on the right.

---

[Mathematica](http://www.wolfram.com/mathematica/) code posted [here](https://gist.github.com/BrianWeinstein/404ba670e95881b66064).

[Additional source](http://www.physicsclassroom.com/class/sound/Lesson-3/The-Doppler-Effect-and-Shock-Waves) not linked above.
