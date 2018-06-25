---
layout: post
title:  PyWeek, PyGameZero, Paperchase and Mu
date:   2018-06-22 16:11:50 +0100
categories: mu pygame pygamezero 
---

<img src="/assets/red_v_blue.gif"/>

[PyWeek](https://pyweek.org/) is a fun, community-organised game-making event /
competition that doesn't take itself too seriously. As the website says, the
PyWeek challenge:

1. Invites entrants to write a game in one week from scratch either as an
  individual or in a team,
2. Is intended to be challenging and fun,
3. Will hopefully increase the public body of game tools, code and expertise,
4. Will let a lot of people actually finish a game, and
5. May inspire new projects (with ready made teams!)

As the name suggests, all entries should be written in Python and incorporate a
theme announced at the start of the challenge.

PyWeek happens a couple of times a year and in April it was organised by my
buddy Dan Pope (aka [lordmauve](https://twitter.com/lordmauve)). Dan has many
claims to Pythonic-fame, but the one I'm going to focus on today is that he's
the creator and maintainer of a wonderful library called
[PyGame Zero](https://pygame-zero.readthedocs.io/en/stable/). As the name
suggests, PyGame Zero is based upon another wonderful library called
[PyGame](http://pygame.org/) (maintained by another equally talented buddy,
[René Dudfield](https://github.com/illume)).
PyGame makes it very easy to create graphical games in Python. PyGame is highly
portable which means that games made with PyGame will run on plenty of
platforms. PyGame Zero is a beginner-friendly wrapper around PyGame.

Dan created PyGame Zero after working with a group of teachers at PyCon UK's
education track. Since he's a gifted and experienced game developer he
was able to create a simple graphical game in about an hour. As he did so, he
explained to the watching teachers exactly what it was he was doing. However,
the feedback from the teachers was clear (paraphrased), "While PyGame might be easy for
you (Dan), the kids we teach would find it hard to put together 10 lines of
Python, let alone the 500 line you just created; we need a way that makes
it easy to create something cool with very little code".

And so, the seeds for PyGame Zero were sown. Dan has created a simple and
easy-to-understand wrapper that enables learners to make something graphical
in only a handful of lines of code. If you're interested in learning
more about PyGame Zero (including a really great tutorial) go check out
the beautifully written [project documentation](https://pygame-zero.readthedocs.io/en/stable/).

Since Mu has a PyGame Zero mode, I thought I'd enter the most recent PyWeek and
try to create my first ever game using just Mu and PyGame Zero. The theme was
"two worlds" and after an ideas generation session (with input from my three
kids) the concept for a game, called Paperchase, was born.

The blurb for the game says...

> The intergalactic war between the red and blue factions of the biro universe
> has reached its climax. Each world has sent a stick-figure champion to race
> in the "Paper chase" for ultimate victory and to decide which colour biro
> pen teachers should use when marking work. (Get 200 steps ahead to win,
> collect up to 3 Python power-ups to import antigravity and avoid all other
> obstacles.)

The [PyGame Zero tutorial](https://pygame-zero.readthedocs.io/en/stable/introduction.html)
shows you how to make an animated alien float across
the screen. I took this as my starting point and, after several hours of
drawing and discarding a huge number of naff-looking stick figures and and
taking about 5 minutes on only a few lines of Python code I had this:

<img src="/assets/running_man.gif"/>

(Interesting aside: I estimate I spent about 80% of my time in PyWeek drawing,
testing and revising game assets like the animations and objects in the game.
Of the remaining 20% of my time, most of it was spent reading PyGame Zero's
excellent documentation to guide me in how to make something or other work.
Time spent actually writing Python code was probably only 5% of the total.)

During PyWeek, participants are encouraged to submit diary entries to
plot their progress and so others can see how they're getting on. This was a
wonderful experience because participants leave supportive
comments on each other's diary entries and even give user-created "awards" (for
instance, I gave one game "Ent of the Year" since the game involved becoming
the spirit of a tree). You can read [my diary entries here](https://pyweek.org/e/ntoll/)
and [all the participant's diary entries are here](https://pyweek.org/25/diaries/).

At the end of the week of coding, participants judge each others' entries and
a winner is declared for both individual and team entries. I'm pleased to say
I placed a respectable [8th out of 23](https://pyweek.org/25/ratings/).

Most importantly for Mu, I was able to try out writing an actual real-life
game with it. The experience was remarkably smooth and it was fun to type
some code and click the "play" button to immediately see the change take
effect. Such a quick turnaround in a write-play-check-change cycle makes coding
games lots of fun. I also quickly appreciated the ability to just copy and
paste the different sorts of game asset into the right locations thanks to 
Mu's shortcuts to the file system.

<img src="/assets/mu_add_image.gif"/>

I'd highly recommend everyone take part in a PyWeek -- it's a fun and
supportive community who are friendly to newbies (such as myself). If you do
take part, please consider using Mu and PyGame Zero!

How did the game turn out? Here's a video of me and my thirteen year-old son
play-testing the game. The source code can be
[found here](https://github.com/ntoll/paperchase).


<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/z_wGpJubVwI?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
