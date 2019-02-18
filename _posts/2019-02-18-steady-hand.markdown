---
layout: post
title:  "A Steady Hand and Heart" 
date:   2019-02-18 13:30:00 +0100
image:  /assets/bigles.jpg
categories: mu users 
---

This post celebrates the extraordinarily talented and inventive friend of Mu,
[Mr. Les Pounder](https://bigl.es/).

<img src="/assets/bigles.jpg"/>

I first met Les at PyCon UK back in 2013. I was coordinating the education
track where we had around 40 teachers and 100 kids turn up over two days. This
was an impossible endeavour for a single person to take on. Happily, the
founding principle of the education track was to bring together, *without
prejudice*, a collaborative and open community of people involved or
interested in Python in education. Les was one of several folks who selflessly
contributed for the benefit of the whole community: be it moving furniture to
turn meeting rooms into classrooms, setting up and configuring equipment,
helping out as a teaching assistant or participating in conversations and
debates around Python in education, Les was making positive contributions. He
was a role model who showed he was open, welcoming and helpful to anyone
who turned up.

Since 2013, Les has built a career on these invaluable, rare and unique
attributes. He writes for various "open source" related magazines, runs and
contributes to educational events, speaks at and continues to contribute to
community events, and creates fun and affordable projects which
often feature the inventive use of components and parts purchased from
[Poundland](https://www.poundland.co.uk/) (a UK based shop where all items cost
£1).

The [following project](https://www.kidscodecs.com/adafruit-test-nerves/),
a CircuitPython twist on the "steady hand" game, is a case in point:

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/-hL1kx9a3Pg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div><br/>

What I love about this project is how Les has created "hardware" that anyone
could build themselves and the code needed to run the project is only 32 lines
of very simple CircuitPython running on an Adafruit
[Circuit Playground Express](https://www.adafruit.com/product/3333):

```
import time
import board
from digitalio import DigitalInOut, Direction, Pull
import audioio

spkrenable = DigitalInOut(board.SPEAKER_ENABLE)
spkrenable.direction = Direction.OUTPUT
spkrenable.value = True

led = DigitalInOut(board.D13)
led.direction = Direction.OUTPUT

wand = DigitalInOut(board.A1)
wand.direction = Direction.INPUT
wand.pull = Pull.DOWN

def play_file(filename):
    print("Playing file: " + filename)
    wave_file = open(filename, "rb")
    with audioio.WaveFile(wave_file) as wave:
        with audioio.AudioOut(board.A0) as audio:
            audio.play(wave)
            while audio.playing:
                pass
    print("Finished")

while True:
    if wand.value:  # button is pushed
        led.value = True
        print(True)
        play_file("buzzer.wav")
        time.sleep(0.5)
```

You can find a treasure trove of these sorts of projects at
[Les's personal website](https://bigl.es/), and the sheer number of such
projects is testament to Les's extraordinary contribution to the wider
community of programmers, educators and learners. Thank you Les for your
amazing work.

But I was recently struck by Les's [most recent blog post](https://bigl.es/when-life-gives-you-lemons/),
in which he describes a series of tragic and unwelcome events in his life. What
made the biggest impression on me was Les's indomitable spirit and unflinching
sense of service to others. As he says, when he concludes his post:

> If you have the means to help someone, even something as trivial as picking
> up something they drop, then do so. If you do not have the means then the
> opportunity will present itself in the future, at a time when you may have
> the means.

I heartily recommend you read the whole article.

We are lucky to have such a talented and big hearted member of our community.
We can all learn from his example. We could all strive to be "more Les".
