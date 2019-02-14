---
layout: post
title:  "A GPIOZero Theramin for Valentine's Day" 
date:   2019-02-14 10:00:00 +0100
image:  /assets/gpio.png
categories: mu users 
---

<img src="/assets/gpiozero.png" style="border: none;"/>

Thanks to [Ben Nuttall](https://twitter.com/ben_nuttall/), one of the
maintainers of the wonderful, [GPIOZero](https://gpiozero.readthedocs.io/en/stable/) library, love is in the air.

Why not serenade your Valentine with Mu, a distance sensor, speaker, Raspberry
Pi and some nifty Python code which uses GPIOZero to turn the hardware into a
romantic Theramin..?

It's only four lines of code, thus showing how easy it is to make cool hardware
hacks with Mu, Python and GPIOZero:

```
from gpiozero import TonalBuzzer, DistanceSensor

buzzer = TonalBuzzer(20)
ds = DistanceSensor(14, 26)

buzzer.source = ds
```

The end result is full of love (for GPIO related shenanigans):

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/4ow5zfkgRMQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div><br/>
