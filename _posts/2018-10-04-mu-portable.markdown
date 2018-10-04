---
layout: post
title:  Making mu Portable
date:   2018-10-04 13:00:00 +0100
image:  /assets/mu-portable.png
categories: mu portable
---

I've been using Mu since it was just an editor for micropython on the BBC micro:bit and I find myself using it nearly every day because of the way it removes all the features I don't need and keeps the ones I do need in a simple layout, so when I started my GCSE Computer Science course, with the first topic being Python Programming, I instantly wanted to use Mu in class. Simple, right? Unfortunately it's not, there is an issue. If you've ever worked in a school before, you'll know about the hassle of getting stuff installed on school computers, it's not easy at all. Even if it's an educational program like Mu that's going to benefit students doing Python Programming in class there are tons of hurdles to jump through to even get in touch with the people who do that sort of thing so this looked like the end of the line for me using Mu in class. I needed to come up with a solution.

So, with a bit of thinking about how I could tackle the issue, the thought came. Why not install Mu on a pendrive, so I got down to work. Unfortnately the computers at school are very locked down so there is no Command Prompt, you can't use Pip, run EXE files, run installers that require Admin roles and many more things that restricted running the installer at school to download Mu at school on a pendrive seemed a no go without breaking some rules, which I was not prepared to do. I had to find another way to install Mu on my pendrive, so I did it at home.

I'd like to introduce Mu-Portable, my solution to running Mu anywhere, i've put Mu in some zip files so that you can download and extract them so you don't have to go through the hassle that I did. Let me explain how I did it.

<img src="/assets/mu-portable.png"/>

## How did I get Mu to install and run on the pendrive?

Firstly I had to install Mu on the pendrive. This is a very simple thing to do, when you run the mu installer, you can select the installation Path, for me it was just a case of selecting the USB drive and installing it direct to the pendrive. 

Once it's installed I faced an issue when I got to school to test it out, when windows detects a drive it assigns a letter (e.g. F:) and this can change when you plug the pendrive in another computer, I had to keep changing the shortcut properties each time and it became a pain, so instead of launching Mu from a shortcut, I created a simple BATCH file that ran everything needed to launch Mu and this runs really well.

## Does Mu actually work? 

Yes! You get the full Mu experience. I've been using it in class for about a week now and it's working really well. It's grabbed lots of peoples attention who have been using IDLE in class and they're now starting to use mu in class too!

## How can I use Portable Mu?

I've uploaded the zip files for people to use, one is for x86 Windows Machines which can be downloaded [here](https://drive.google.com/file/d/1USt4uCrWCXdyJh8byVen1ZkChqnINh7K/view?usp=sharing) and another for x64 Windows Machines which can be downloaded [here](https://drive.google.com/file/d/1as_sP0_c1kSimUqDWVkG3yHJFjHXoUHM/view?usp=sharing). It's just a case of downloading the zip and extracting it onto the pendrive. Once you've done that, double click the Launch Mu file and a window will pop up and you'll see Mu load, it may take some time depending on how quick your computer is. 

I hope you find mu-portable useful just like I have, it's  not only handy for schools but even more so for having a portable version of Mu to take with you anywhere you go, whether that be when going to a friends house or using a library computer, so why not download it and share the power of Mu with even more people who maybe can't install things on their computer!