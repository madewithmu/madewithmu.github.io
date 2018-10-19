---
layout: post
title:  The Blackpool Chainsaw Massacre!
date:   2018-10-19 21:30:00 +0100
image:  /assets/chainsaw.jpg
categories: mu users 
---

Fellow MU-tant (geddit?) [Les Pounder](https://twitter.com/biglesp), has a 
[stonking project](https://bigl.es/friday-fun-adafruit-chainsaw/)
for Halloween trick-or-treating, made with an
[Adafruit Circuit Playground Express](https://www.adafruit.com/product/3333)
board, CircuitPython and Mu. It's too cool not to re-blog! The video below
shows you all you need to know.

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/__TrBKYVKgw" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
<br/>

Regular readers will know that Les's projects are fun, playful, cheap to build
and easy to assemble. Furthermore, not only has Les a gift for thinking up
such stonking project ideas, but he's a virtuoso mentor when it comes to
explaining how to recreate such projects for yourself. Where am I going with
this?

**If you are a teacher, Les's blog is a GOLDMINE of ideas, resources and
projects for use in your own classroom.**

In this case, the parts are all from [PoundLand](https://www.poundland.co.uk/)
(no relation), and the digital assets are an audio file and the following
short Python script:

```
import audioio
import board
from digitalio import DigitalInOut, Direction, Pull

# enable the speaker
spkrenable = DigitalInOut(board.SPEAKER_ENABLE)
spkrenable.direction = Direction.OUTPUT
spkrenable.value = True

# make the input trigger
trigger = DigitalInOut(board.A1)
trigger.direction = Direction.INPUT
trigger.pull = Pull.DOWN

#Create a function to play audio files.
def play_file(filename):
    print("Playing file: " + filename)
    wave_file = open(filename, "rb")
    with audioio.WaveFile(wave_file) as wave:
        with audioio.AudioOut(board.A0) as audio:
            audio.play(wave)
            while audio.playing:
                pass
    print("Finished")

#Main Loop, press a button...make noise!
while True:
    if trigger.value:
        play_file("sound.wav")
```

What are you waiting for?
