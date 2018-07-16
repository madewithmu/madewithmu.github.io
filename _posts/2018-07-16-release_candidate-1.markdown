---
layout: post
title:  Mu Release Candidate
date:   2018-07-16 18:25:00 +0100
image:  /assets/hello_18n.png
categories: mu releases 
---

The [release candidate for Mu 1.0.0](https://codewith.mu/en/download) is out!
This is the last step before the
final release of Mu 1.0. Apart from a few minor bug fixes, the biggest change
from beta 17 is the inclusion of various translations for the user interface.
Full details can be found in the [change log](https://mu.readthedocs.io/en/latest/changes.html#rc-1).

<img src="/assets/hello_i18n.png"/>

Many thanks to the following people for their magnificent work on the following
translations:

* Chinese (incomplete), by [Pydo](https://github.com/yonghuming).
* Japanese, by [Minoru Inachi](https://github.com/MinoruInachi).
* French, by [Gerald Quintana](https://github.com/gquintana).
* Spanish, by [Carlos Pereira Atencio](https://twitter.com/carlosperate).
* Portuguese, by [Tiago Montes](https://twitter.com/setnomt).

I would love to include **more** translations in the final release, especially
if they're one of the following:

* Arabic
* German
* Greek
* Hebrew
* Hindi
* Italian
* Russian

(This list reflects both reach and accessibility of languages so Mu is usable
by as many beginner programmers as possible.)

Other highlights include a fix to allow users of Adafruit devices to save a
file called `code.py`. This was getting erroneously caught by the new "shadow
module" feature which, in this specific case, doesn't apply. Zander Brown
continues to make extraordinary progress in making the user interface both
great to look at *and* consistent across all platforms. We had quite a bit of
feedback from teachers who value such UI consistency: it allows them to create
resources that apply to all platforms, thus avoiding all the
complications of, "if you're on `<platform>`, then this will look different"
interruptions in the flow of such resources. Finally, Tim Golden and
Jonny Austin have done sterling work testing the various fixes for problematic
edge-cases in the new BBC micro:bit flash functionality.
