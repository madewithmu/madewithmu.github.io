---
layout: post
title:  "Awesome Adafruit: Python, Lasers and Mu!"
date:   2018-10-08 21:30:00 +0100
image:  /assets/lasers.png
categories: mu users 
---

[Limor 'Ladyada' Fried](http://www.ladyada.net/), founder of
[Adafruit](https://adafruit.com/) and maker extraordinaire, has just released
a video demonstrating [LIDAR](https://en.wikipedia.org/wiki/Lidar)
(laser based distance measurement) with
[CircuitPython](https://learn.adafruit.com/category/circuitpython) and Mu.

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Vgft9Xl836A?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div><br/>

The source code and documentation for the library Limor demonstrates can be
found [on GitHub](https://github.com/adafruit/Adafruit_CircuitPython_LIDARLite).
Under the hood, it's an I2C based API which has beed abstracted into something
Pythonic. The code example included in the README (reproduced below)
demonstrates how easy it is to use the LIDAR sensor with CircuitPython. In only
a few lines of code it outputs data which Mu can use with its built-in plotter:

```
import time
import board
import busio
import adafruit_lidarlite

# Create library object using our Bus I2C port
i2c = busio.I2C(board.SCL, board.SDA)

# Default configuration, with only i2c wires
sensor = adafruit_lidarlite.LIDARLite(i2c)

while True:
    try:
        # We print tuples so you can plot with Mu Plotter
        print((sensor.distance,))
    except RuntimeError as e:
        # If we get a reading error, just print it and keep truckin'
        print(e)
    time.sleep(0.01) # you can remove this for ultra-fast measurements!
```

Great stuff!

It's at this point in geeky blog posts that it's traditional to bring up
[sharks, lasers and Dr.Evil](https://www.youtube.com/watch?v=60AjI1pIzVQ).
Happily, I ironically understand apophasis. ;-)
