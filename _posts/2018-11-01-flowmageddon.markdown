---
layout: post
title:  "Mu and PyWeek: Traffic Flowmageddon"
date:   2018-11-01 11:00:00 +0100
image:  /assets/flowmageddon.png
categories: mu users 
---

Last week was [PyWeek](https://pyweek.org/), where entrants have a week to make
a game on a given theme using Python. Myself and my buddy
[Andrew Smith](http://http://andrewsmithauthor.com/) decided to form a
team called [Code to Joy](https://pyweek.org/e/code-to-joy/) and write
something using Mu and
[PyGameZero](https://pygame-zero.readthedocs.io/en/stable/). At the start of
the week the theme was revealed as "flow". We ended up creating
"Traffic Flowmageddon" with gameplay like 80's classic
[Frogger](https://en.wikipedia.org/wiki/Frogger), a look similar to the
90's classic [Grand Theft Auto](https://en.wikipedia.org/wiki/Grand_Theft_Auto_(video_game))
and with a dash of [Shaun of the Dead](https://en.wikipedia.org/wiki/Shaun_of_the_Dead)
thrown in for some timely Halloween spice. The opening screen pretty much sums
up the character of the game:

<img src="/assets/flowmageddon.png"/>

It was fun to work in a team. I mainly concentrated on the code and Andrew
spent time on the sound effects and music. The graphical assets were either
bodged together by us or were free-to-use downloads from the internet. What was
particularly pleasing was how quickly we were able to put together the
scaffolding of the game in a very short period of time and just under 100
lines of Python:

<img src="/assets/flowmageddon1.gif"/>

Yes, that's quite an abstract looking game (none of the graphical assets had
been created), but the labelled boxes and fact that stuff is moving around
demonstrated the core of the game worked well. Having said that, simply adding
some proper graphics and an animation on the hero sprite that the player
controls makes a huge difference! It actually looks like a game:

<img src="/assets/flowmageddon4.gif"/>

At this point in the development of the game, one of us had the idea of adding
zombies and, since I'd been tweeting about our progress, we were getting
suggestions for other features from friends (such as potholes in the road which
would slow you down, or drivers with no lane discipline).

The zombies make a big difference since they force you off the pavement and
into the flow of traffic.

<img src="/assets/flowmageddon5.gif"/>

In the meantime, Andrew had been putting together music and sound
effects as well as the code to load and play them at the appropriate moments
in the game. This was especially rewarding to hear since sound and music add
so much to the atmosphere. Andrew found some appropriately
spooky sounding music, a "happy tune" to play when the game completed and a
whole host of sounds for the zombies and traffic (for example, if you get too
close to one of the London taxi cabs, the driver will shout at you).

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/08mvNmhOVG4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div><br/>

As the video shows, the finished game works quite well for something cobbled
together in just a week. Most importantly, it's all done with Mu and PyGameZero
in around [400 lines of Python](https://github.com/ntoll/traffic_flowmageddon).

I'd heartily recommend anyone participate in future PyWeeks. The organiser,
[Dan Pope](https://twitter.com/lordmauve) (who also created PyGameZero) has
done a fantastic job of creating such a fun competition with a community of
coders creating such joyously goofy games.

Long may it last!
