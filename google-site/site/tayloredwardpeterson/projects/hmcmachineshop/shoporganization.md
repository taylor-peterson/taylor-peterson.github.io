---
layout: default
title: Shop Organization
---

[Overview](/projects/hmcmachineshop)

[Shop Reform](/projects/hmcmachineshop/shopreform)

[Shop Organization](/projects/hmcmachineshop/shoporganization)

[Prof Hammer](/projects/hmcmachineshop/profhammer)

[CNC Mill Collet Holder](/projects/hmcmachineshop/cncmillcolletholder)

A big part of our work in the shop has been improving organization. Typically, this has been done by implementing visual controls. For example, putting tools on pegboards and tracing their outlines so it's clear what's missing. Another thing we've done is arrange all work stations such that they now contain all tools used in common use such that everything is clearly visible and missing tools stand out. Mill station 2, as shown below is a great example of this. 

[![](https://docs.google.com/uc?id=0B0Jfms0twG8EaERsaS1mYzJmRmM&export=download)](https://docs.google.com/file/d/0B0Jfms0twG8EaERsaS1mYzJmRmM/edit?usp=drive_web)

Mill station 2. 

Another major change we made was to add cameras to each shop. After some setup (including routing a couple hundred feet of ethernet cable through the ceilings) we had a monitor setup in the main shop which allows proctors to monitor activity in the other two shops. While this by no means obviates the need to physically go to the other shops to check on students, it's definitely better than in the best when proctors had no idea what was going on in the other shops. 

After getting fed up with the old check in system (which consisted of manually checking if a student was cleared on a spreadsheet hosted on a very, very slow computer), I took lead creating an automated check-in system (joined by Richard Piersall and later on Alex Ozdemir). A mostly complete version of the system may be seen below. 

[![](https://docs.google.com/uc?id=0B0Jfms0twG8EWE5HYzJLRDFSZTA&export=download)](https://docs.google.com/file/d/0B0Jfms0twG8EWE5HYzJLRDFSZTA/edit?usp=drive_web)

The front of the check-in board showing several IDs in place. 

The system works by taking user input via buttons and a card swipe. This information is transmitted to a computer running a python script which communicates with the Google spreadsheet containing the shop user list. The process of checking in a user is reduced to a few button presses and card swipes. While there's still a ways to go to smooth out the kinks as of now, the system has some huge benefits that make it worth all the work (e.g. tracking shop usage, being able to display machine use live). 

Making the board itself was definitely a hassle. As you can see in the image of the back of the board below, there are a ton of pieces involved. In particular, getting the plastic panels to sit flat and properly adjusting all of the microswitches were major pains. 

[![](https://docs.google.com/uc?id=0B0Jfms0twG8ESG9Nc3JiT2lfclU&export=download)](https://docs.google.com/file/d/0B0Jfms0twG8ESG9Nc3JiT2lfclU/edit?usp=drive_web)

The back side of the check-in system. 
