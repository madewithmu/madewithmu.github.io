---
layout: post
title:  Shhh! Hunting micro:bits in a Library with Mu
date:   2018-07-13 09:00:00 +0100
image:  /assets/iis_student.jpg
categories: mu users 
---

I had a *stonking* time yesterday afternoon with [Harvey Sharman](https://twitter.com/BitawsBrackley),
who runs workshops for young coders in a library close to where I live. This
particular afternoon was spent in the company of a group of eager
eleven-year-olds. Harvey's learning activity? Use Mu to program "transmitter"
and "detector" micro:bits so the kids could organise a treasure hunt in the
library. Let joyful coding chaos ensue!

I first became aware of Harvey's work via the following tweet:

<img src="/assets/iis_student.jpg"/>

<blockquote data-lang="en"><p lang="en" dir="ltr">One of my pupils inspired in Python Mu hard coding the International Space Station project to collect live data of latitude and longitude coordinates to locate the actual position of the space station using an A3 print of the global map with coordinates. <a href="https://twitter.com/ntoll?ref_src=twsrc%5Etfw">@ntoll</a> 🛰️ <a href="https://twitter.com/rebeccafdp?ref_src=twsrc%5Etfw">@rebeccafdp</a> <a href="https://t.co/Ke2JKzDiju">pic.twitter.com/Ke2JKzDiju</a></p>&mdash; Harvey Sharman (@BitawsBrackley) <a href="https://twitter.com/BitawsBrackley/status/1012386409460764673?ref_src=twsrc%5Etfw">June 28, 2018</a></blockquote>

It was a stroke of luck that I live in the next village from Harvey and I just
had to investigate. As a result I was invited to observe Harvey and
his students in action.

The group of eleven-year-olds sped through the task of writing the code,
checking it and flashing it onto the micro:bit. Then the group split in two:
half were unleashed into the wider library to hide their "transmitter"
micro:bits and upon their return the other half were let loose, waving around
poles with their "detector" micro:bits stuck on the end. If the "detector" got
close to a "transmitter" it would start to bleep and the "X" on the micro:bit's
display changed to a number to indicate the relative proximity of the devices.

Imagine, if you will, a sleepy afternoon at
[Brackley library](http://www3.northamptonshire.gov.uk/councilservices/library-service/visiting-your-library/list-of-libraries/Pages/brackley-library.aspx):
the knitting circle quietly
click-clacking in one corner, a pensioner's jigsaw club (armed with tea and
biscuits) in yet another, and a hoard of enthusiastic eleven-year-olds waving
around blinking and bleeping poles at anything and everything (including the
afore mentioned knitting circle and jigsaw club) in an attempt to
find "treasure".

To say the kids had a huge amount of fun is an understatement (to their credit,
the other library users were very patient and I was especially pleased to
see maniacal grins on the faces of the librarians as the kids explored
all the various sections of the library). Public libraries are such an asset to
our communities since they're the only place the pensioner's jigsaw club could
rub shoulders with eleven-year-olds from a code club. Two different parts of
the same community got to see what each other were doing.

Afterwards, when the kids had left, we recorded the following video to explain
how things work:

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/cLJkUV6zH9g?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div><br/>

The source code is very simple and takes only minutes to type in. The detector
works by checking the strength of radio signals. The stronger the signal of a
received message the closer you are (and the higher the number displayed and
the bleeps from the speaker). The transmitter micro:bits constantly send out
signals at the lowest possible power so the their signal is only detected when
you're stood close by (I'd say around 3 to 4 meters). This is beautifully
simple and ingenious and could form the basis for all sorts of interesting
classroom activities and learning opportunities. How might you improve the
code?

{% highlight python %}
# Code for the "detector" microbits. Make sure
# a speaker is attached in the usual way.
from microbit import *
import radio
import music

radio.config(channel=10)
radio.on()

while True:
    message = radio.receive_full()
    if message:
        strength = message[1] + 100
        displaystrength = int((strength / 10) + 1)
        display.show(str(displaystrength))
        music.pitch(strength * 50, 100)
    else:
        display.show(Image.NO)
{% endhighlight %}

{% highlight python %}
# Code for the "transmitter" microbits.
from microbit imort *
import radio
id = "10"
display.show(id)
radio.config(power=0)
radio.config(channel=10)
radio.on()

while True:
    radio.send(id)
{% endhighlight %}

Harvey tells me that Mu makes Python programming easy for his young coders and
my own observations during the workshop confirm this. It took moments for the
kids to figure out what to do. It was also cool to see them help each other and
make suggestions for using Mu. For instance, once one kid figured out how to
use the autocomplete functionality to avoid typing long words, they
were all at it after the inevitable, "hey, look at this!".

I look forward to more projects, games and "hacks" from Harvey and
his young charges (and I'll keep you posted!).
