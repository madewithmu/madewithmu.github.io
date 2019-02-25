---
layout: post
title:  "Student Made Stress Management Mask" 
date:   2019-02-25 08:15:00 +0100
image:  /assets/stress-buster.jpg
categories: mu users 
---

[Sean Tibor](https://twitter.com/smtibor), a teacher based at
[Pine Crest School](https://www.pinecrest.edu/) in Boca Raton,
Florida, has been in touch about a [cool project](https://github.com/seantibor/stressmanagementmask)
created by one of his students called Dilnaam D.

Sean is one of the co-hosts (along with his colleague
[Kelly Schuster-Pared](https://twitter.com/KellyPared)) of the excellent
[Teaching Python podcast](https://www.teachingpython.fm/). I've been working
through the available episodes and constantly find myself grinning like the
Cheshire Cat as I'm reminded of my own experiences as a teacher (of music), and
learn how this talented duo of pedagogical pros practice the art of teaching
technology, and especially Python. I heartily recommend you take a listen.

Onto the intriguing student project...

Dilnaam's 
[project](https://github.com/seantibor/stressmanagementmask) is a sort of
interactive face mask, made with an
[Adafruit Circuit Playground Express](https://www.adafruit.com/product/3333),
[CircuitPython](https://www.adafruit.com/category/956) and Mu. The mask allows
folks to become aware of and manage their stress levels (very useful for
teachers!). Dilnaam explains:

> This mask was made to demonstrate how a CircuitPlayground Express could be
> used to measure body temperature and indicate stress levels. My theory is
> that body temperature is an indicator of stressful feelings and that people
> can better control their stress when they have a visual indication of their
> own stress state.

In the picture below, we can see see Sean bravely acting as a test subject
as (presumably) Dilnaam looks on while making adjustments to the code in Mu.
A teacher acting as a test subject for their students shows a wonderful sense
of trust. This is great to see! :-)

<img src="/assets/stress-buster.jpg"/>

This scene reminds me of [Wallace and Gromit](https://wallaceandgromit.com/),
where the silent, loyal and infinitely patient [Gromit](https://en.wikipedia.org/wiki/Wallace_and_Gromit#Gromit)
aids the cheese obsessed [Wallace](https://en.wikipedia.org/wiki/Wallace_and_Gromit#Wallace)
in testing intriguing inventions made from advanced technology and
household items cleverly put together in unexpected ways (usually with
unfortunate repercussions for poor old Gromit). However, I notice the Circuit
Playground Express board attached to the side of Sean's head is glowing green,
demonstrating the test was a success (well done Sean for being such a chilled
out test subject).

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/_6g8WGpMstI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div><br/>

Dilnaam's code is beautifully simple and I love the helpful comments. I'm
especially pleased Mu's 
[plotter feature](https://codewith.mu/en/tutorials/1.0/plotter) is used to
monitor the test subject's temperature.

{% highlight python %}
from adafruit_circutplayground.express import cpx
import time

while True:
    # get the temperature in F
    temp = cpx.temperature * 9 / 5 + 32
    print((temp,))  #Farenheight output for Mu plotting
    time.sleep(0.5)
    if temp > 91: # This is my initial theory for the stress levels and temperature
        cpx.pixels.fill((255,0,0))
    elif temp < 90:
        cpx.pixels.fill((0,255,0))
{% endhighlight %}

Finally, here's Dilnaam's hardware, in all its glory.

<img src="/assets/stress-mask.jpg"/>

Dilnaam, those of us who make Mu would like to congratulate you on such a
wonderfully simple yet intriguing project. Keep up the great work! We look
forward to hearing about the amazing things you and your classmates invent in
the future.

:-)
