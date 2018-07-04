---
layout: post
title:  "Blinky, Bloopy 4th July"
date:   2018-07-04 10:00:00 +0100
image:  /assets/morse.gif
categories: mu submitted
---

[Keith](https://github.com/KFW) has created a colourful and noisy project with
Mu and an Adafruit
[Circuit Playground Express](https://www.adafruit.com/product/3333) (CPE)
board. Just what you need for the 4th July!

<img src="/assets/morse.gif"/>

By day Keith is a healthcare informatics professional. By night, like many
of us, he builds robots and other Maker-type projects. This particular project
blinks different messages in Morse code. You can configure the LED colour as
well as toggle the buzzer (so the board "bloops" Morse code too).

He says, "I love the idea that I could use Python to program a
microcontroller" and explains the origin of the project as follows:

> I was at the San Mateo Maker Faire this year (I was at the first one, and
> have been there or NYC Maker Faire every year since). I had brought the CPE
> with me to play with in case I had any free time (I hadn't had time to really
> mess with it - big project at work). My flight Sunday night was cancelled, so
> I thought I might go to the [Bring-a-Hack event](http://blog.oshpark.com/2018/04/13/bring-a-hack/).
> I didn't want to show up empty handed, but all I could think up was a lame
> demo of the CPE. I quickly re-reviewed some tutorials, and wrote a quick
> program in my hotel room. Didn't work at all. Tried different things,
> cut-and-paste sample code (which all worked), finally gave up. At that point
> I was tired, and had to get up early for a flight, so I canned it. When I got
> back to St. Louis and read through the code again, I realized I had thought
> that time.sleep was in milliseconds (like Arduino Delay), rather than in
> seconds. The original code I had written was actually fine - just a thousand
> times slower than I was expecting. Once I fixed that, it was fine. I've
> since cleaned it up a little.

Thus proving the old adage that, "good things come to those who wait". ;-)

Keith has helpfully provided a video of his code in action:

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/EHyXZPKgJ-s?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div><br/>


The [project's source code](https://github.com/KFW/LAME) contains a complete
implementation of a Morse code transmitter that could form the basis for many
future beginner-friendly projects. If you're interested in
changing the transmitted messages you should modify lines
[92](https://github.com/KFW/LAME/blob/master/code.py#L92) and
[95](https://github.com/KFW/LAME/blob/master/code.py#L95). The Morse code
definition is in a Python dictionary on line [22](https://github.com/KFW/LAME/blob/master/code.py#L22)
and the loop, starting on line [98](https://github.com/KFW/LAME/blob/master/code.py#L98),
is a great example of how to convert characters into Morse code. Check it out!

I wonder, how hard might it be to implement simple signal processing
using the Circuit Playground Express's microphone or light sensor to detect the
message transmitted from a second device and emit the result to the
CircuitPython REPL? (That's a trick question... it's very easy, but I leave it
as an exercise for the reader to solve.)

As for Mu, Keith says it is, "certainly convenient for programming the CPE (and
BBC micro:bit). The biggest thing I miss is a keyboard shortcut to
comment/uncomment bits of code. That would make troubleshooting so much
faster." Check out progress for this feature request on our
[issue tracker](https://github.com/mu-editor/mu/issues/516).

Thank you Keith for such an easy-to-follow Morse code project!

Everyone else, if you extend or re-use this code, let us know! We love to shine
a light on the hard work of Mu users (no pun intended). :-)
