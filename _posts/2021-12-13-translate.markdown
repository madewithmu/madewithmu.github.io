---
layout: post
title:  "A Request for Help: Translations please!"
date:   2021-12-13 17:00:00 +0100
image:  /assets/icon.png
categories: mu users 
---

**UPDATE: Coordination of translations is being done [via this discussion on GitHub](https://github.com/mu-editor/mu/discussions/1931).**

<img src="/assets/mu_in_chinese.png"/>

Education is a right, not a privilege.

It means that access to education should be as easy as possible given the
different and diverse circumstances of learners.

The lingua franca of coding is
English, and most programming languages (Python included) use English for its
keywords (`if... else`, `for ... in ...` and `while ...` for instance). Most
programming tutorials, tools and resources are written in English. But what if
English is an additional language for you, or, especially if you're an
absolute beginner, you don't know English at all?

Clearly, you'll face challenges learning Python.

This is where [translating Mu](https://github.com/mu-editor/mu/discussions/1931) comes into play. We _care very
deeply_ that learners are able to take their first steps with
Python in a tool that works in _their language_. We try
very hard to meet learners where they are, and that includes their native
language and being culturally sensitive through our user interface.

If you have any doubt of the importance of
this sort of thing, here's a wonderful video of some young Chinese students
saying thank you for being able to learn Python in Mu...

<div class="video-container">
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/w3hQglx5Kj0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div><br/>

Thanks to the remarkable work of both [Vasco](https://github.com/xbecas) and
[Tiago](https://github.com/tmontes), our translation strings have been updated
again and include all the new written elements of our user interface that have
not yet been translated (i.e. those added during the development of version
1.1). Existing translations that require updates
[can be found in the `locale` directory](https://github.com/mu-editor/mu/tree/master/mu/locale)
and, if you're looking for an example of the sorts of update we're looking for,
you can't go far wrong looking at Vasco's
[update of the Portuguese translation](https://github.com/mu-editor/mu/pull/1795).

If you want to add a translation for a _new_ language, you should use the
following convenience commands now built into our Makefile:

```
make translate_begin LANG=xx_XX - create/update a mu.po file for translation.
make translate_done LANG=xx_XX - compile translation strings in mu.po to mu.mo file.
make translate_test LANG=xx_XX - run translate_done and launch Mu in the given LANG.
```

If you're looking for a fun way to contribute to Mu, this is it. We're a
friendly team and you can ask questions via
[our Gitter channel](https://gitter.im/mu-editor/general)
or via a 
[pull request on GitHub](https://github.com/mu-editor/mu/pulls).

**Coordination of translations is being done [via this discussion on GitHub](https://github.com/mu-editor/mu/discussions/1931).**

This is the last work needed in our codebase for us to release version 1.1.

We look forward to your contributions and thank you in advance.

:-)
