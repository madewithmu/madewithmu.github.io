---
layout: post
title:  Mu and PyGameZero Gamepad Demo
date:   2018-09-12 18:30:00 +0100
image:  /assets/gamepad.png
categories: mu users 
---

Anthony Briggs (who blogs at [NeoLudic](http://neoluddic.tumblr.com/)) got in
touch [via Twitter](https://twitter.com/AnthonyBriggs/status/1039070401366650880)
with a proof-of-concept for controlling PyGameZero games with
a gamepad (such as the one you'll use with your XBox or Playstation).

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/b2IPNCJtUL4?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div><br/>

The [source code](https://gist.github.com/AnthonyBriggs/f8b4d53cf9387e73fab5badb9cc06417)
is nice and simple, although it relies an two patches which have not yet made
it into a release of PyGameZero (so mark this as coming soon). One patch adds
joystick support (i.e. what you do with the gamepad) and the other makes it
easy to flip sprites.

Coming soon to a PyGameZero/Mu release near you!
