---
layout: post
title:  Adafruit, CircuitPython and Mu
date:   2018-06-24 12:17:00 +0100
categories: mu adafruit circuitpython
---

[Adafruit](https://adafruit.com/), the brainchild of
[Limor 'Ladyada' Fried](http://www.ladyada.net/), was founded to create the
best possible resources, boards and designs for learning about electronics and
programming. Over the last decade she and her colleagues have surpassed their
initial goal and become the touchstone for inspiring a community to engage with
making electronic devices for serious, playful and educational use. Perhaps
most importantly, Limor and her colleagues have become worthy role models to
many for whom electronics or programming may, at first, appear "not for them".
They have been celebrated by the [WhiteHouse](https://blog.adafruit.com/2017/02/23/ladyada-adafruit-makers-removed-from-whitehouse-website-whchamps-nationofmakers-mfgday-makerswomen/),
written about in high profile magazine articles (such as for
[WIRED](https://blog.adafruit.com/2011/03/16/thank-you-makers/)
and [MAKE](https://blog.adafruit.com/2017/05/08/limor-ladyada-fried-on-the-cover-of-make-magazine-makev57/) magazines)
and been the recipients of [several](https://www.inc.com/profile/adafruit-industries)
[awards](https://blog.adafruit.com/2012/12/18/adafruits-ladyada-limor-fried-named-entrepreneur-of-the-year-by-entrepreneur-magazine-entmagazine/).

They are fearless in their support for and promotion of under-represented
groups in technology. As they say on their website,

> ... we’ll do our best to shine a light on the untold stories of women in
> STEM and underrepresented champions from all over the world.

Happily, Adafruit support their own flavour of
[MicroPython](https://micropython.org) (think of it like an Adafruit "distro"
of MicroPython) called [CircuitPython](https://learn.adafruit.com/category/circuitpython).
CircuitPython provides a uniform and consistent API for all the many and growing
number of Adafruit boards that it supports. This makes it very easy to transfer
your skills and knowledge between different types of device, be it a minute
[Gemma](https://learn.adafruit.com/adafruit-gemma-m0/circuitpython) board or
the spectacularly colourful and feature-ful [Circuit Playground Express](https://www.adafruit.com/product/3333).

<p><video id="Slide1" preload="auto" muted="" loop="" autoplay="" poster="https://cdn-shop.adafruit.com/product-videos/1024x768/3333-05.jpg" width="100%">
<source src="https://cdn-shop.adafruit.com/product-videos/1024x768/3333-05.mp4">
<img src="https://cdn-shop.adafruit.com/product-videos/1024x768/3333-05.jpg">
</video></p>

Mu has a CircuitPython mode which understands how the boards work (for example,
you store your source code on the connected device's USB storage). It also
provides a couple of short-cut functions to help you interact with your
CircuitPython device. For example, reading from and interacting with the
connected device's serial connection is but a button press away:

<img src="/assets/adafruit_serial.gif"/>

Perhaps my favourite feature is the plotter, which allows you to visualise data
coming from the connected device. The plotter was
originally [contributed by Limor herself](https://github.com/mu-editor/mu/issues/311).
The following video shows Limor explaining how to visualise the data coming
from the light sensor of a Circuit Playground Express with the plotter built
into Mu (originally blogged
[here](https://learn.adafruit.com/sensor-plotting-with-mu-and-circuitpython?embeds=allow)):

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/8zCRmguw-_c?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div><br/>

What's really great about this example is how short the Python code is:

{% highlight python %}
import time
import analogio
import board

light = analogio.AnalogIn(board.LIGHT)

while True:
    print((light.value,))
    time.sleep(0.1)
{% endhighlight %}

There are plenty of projects and videos for using CircuitPython and Mu on
[Adafruit's website](https://learn.adafruit.com/category/circuitpython).

Check it out..! If you create something awesome, please tell us about it! :-)
