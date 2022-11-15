---
layout: post
title:  "Mu: An Editor in Hostile Environments"
date:   2022-11-14 09:00:00 +0100
image:  /assets/icon.png
categories: mu users 
---

<img src="/assets/venera14.jpg"/>

This is a picture of the surface of Venus, taken by the Soviet
[Venera 14 probe](https://en.wikipedia.org/wiki/Venera_14). Apparently, the
temperature of the barren rocky surface is 465 °C and the pressure is that
of 94 Earth atmospheres (9.5 MPa). The atmosphere is a murky orange, contains
substantial quantities of hydrogen sulphide (so it smells like rotten eggs) and
it rains sulphuric acid. No wonder the probe lasted only 57 minutes before
breaking.

This is, undoubtedly, a hostile environment.

Mu is an editor for beginners. By definition, our users probably don't know
what they're doing (they're beginners!) and, it is with some trepidation, that
we design Mu to work in all sorts of different environments... some of which
are hostile.

For instance, we were once contacted by a teacher who explained that Mu didn't
work on their classroom computers. Mu core contributor
[Tim Golden](http://timgolden.me.uk/) took up the challenge and liaised with
the school's network administrator who had installed Mu. It
turns out they had deliberately configured the student's home directory to be
read only. As many of you will undoubtedly know, a user's home directory is
supposed to be writeable to the user (and any applications they
run, like Mu). Having a writeable home directory is how we save your code,
settings and the log files that help us debug what has happened when Mu
doesn't work.

It would be very easy to mock such a set-up and criticise the school's network
admin as incompetent, ignorant or a clown. But a far more helpful and
compassionate response is to engage with and try to understand the situation.

Tim embodied this approach with great aplomb.

As I remember the details, students all saved their work on a networked drive
and the home directory (containing configuration files) was locked down so they
couldn't change their settings. Unfortunately, Mu's algorithm for discovering
the correct path for the user's home directory was unable to distinguish that
the actual home directory was read only (why would it be?) or that some other
network attached drive was really where students had write permissions.

At the core of this situation is a simple fact: schools are complicated and
often chaotic places.

Lessons were disrupted because the applications
students needed to use were broken because students misconfigured them. The
answer: _don't let students save configuration_.

Hey presto, problem solved... until Mu arrived.

In the end I believe Tim discussed other possible solutions around the core
problem and put guard code in place to ensure Mu would at least helpfully
recover in such a rare and unusual situation. Put simply, if we dealt
with every pathological situation, Mu itself would become pathological software
as it drifted away from simplicity and ease to coping with all possible
situations. Tim's approach is a good example of our alternative: we try very
hard to keep Mu simple and easy while helping
our (beginner) users identify when they run up against a
pathological situation if Mu encounters a problem.

Relatedly, a common solution to problematic configuration is to create a sort
of virtual sandbox isolated from other aspects of the system.

In the Python world we use the `pip` command to install packages, and we wanted
the new version of Mu to provide users with an easy-to-use and simple interface
for this command. My first attempt at a solution involved adding a directory
to the Python path used by Mu and instructing `pip` to use *that* as the
destination for all packages. This mostly worked but not enough of the time
that it was reliable.

Over a friendly coffee in London Tim (again) stepped up to help.

He asked me if there was an aspect of Mu that needed attention but which I
didn't have time to properly tackle. He explained he could own this part of the
codebase, thus giving me some time back to concentrate on all the other things
that needed doing. I explained the Mu and `pip` problem and we quickly came to
the conclusion that we should use the built-in capability of Python to create
virtual environments: isolated Python sandboxes into which packages could be
installed with no problems.

You can probably guess where this is going...

It turns out there are two ways to manage Python virtual environments: the
built-in `venv` module and the third-party `virtualenv` package. Furthermore,
it turns out that automatically creating isolated Python environments isn't
quite as easy as one might think.

In exactly the same way we assumed a user's home directory would always be
writeable, our assumptions about users' computers and the naïveté of
"just automate the use of a virtual environment" opened up a veritable can of
worms. While this approach worked fine for most people, there were significant
numbers of edge cases, each of which required investigation and a solution.

Let's be honest here, asking a beginner to investigate this sort of technical
problem feels like trying to do a [talk down aircraft landing](https://en.wikipedia.org/wiki/Talk-down_aircraft_landing),
yet Tim is both determined and a gifted technical communicator. Over the course
of a few months Tim was able to engage with many confused beginner developers
(along with a few highly experienced coders who'd also stumbled upon Mu) to
iron out the problems when creating a virtual environment for users.

<img src="/assets/splash_screen.gif"/>

In case you're wondering, it is this process that happens on first run of Mu
(which is why Mu takes significantly longer at this moment). It's also why we
engaged with long-time friend of Mu and Pythonic designer extraordinaire
[Steve Hawkes](https://www.dev.ngo/) to produce the funky animation of
Penelope the Python (our mascot).

The end result is, we hope, an opportunity to introduce our users to the
personality of Mu, while also doing a bunch of rather complicated house-keeping
on their behalf.

Of course, Tim doesn't have super powers and there are still kinks to be ironed
out. For instance, there is a [bug in Python itself](https://bugs.python.org/issue46686)
(over which we have no control) which causes perhaps 90% of our current bug
report traffic. While we could work around the issue (it just so happens that
Tim is also a core Python developer and Windows expert, so one of the handful
of engineers on the planet with enough depth of knowledge and context to
understand exactly what would need to be done), the "correct" solution is for
it to be fixed in Python.

Such are the challenges faced by Mu (and its developers, such as Tim) as we try
to make it work as simply as possible for our users, no matter their computing
environment.
