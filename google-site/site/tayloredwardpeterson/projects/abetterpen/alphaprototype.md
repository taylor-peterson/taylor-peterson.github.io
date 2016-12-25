

---
layout: page
title: Prototyping
---

  

| 
  

[Overview](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen)

  

[Problem Statement](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/problemstatement)

  

[Preliminary Design](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/preliminarydesign)

  

 Component Selection 

 Â Â Â [Ink Cartridge](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/cartridgeselection)

 Â Â Â [Clip Screw](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/clipscrewselection)

  

[Prototyping](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/alphaprototype)

  

 "Mass" Production 

 Â Â Bill of Materials 

 Â Â [Process](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/process)

 Â Â Drawings/Parts 

 Â Â [Lessons Learned](https://sites.google.com/site/tayloredwardpeterson/projects/abetterpen/lessonslearned)

 | 

 Generating CAD from preliminary design 

  

 Body 

- CAD model of Pilot G2 0.38 
- This dictated internal diameter to be nominal G2 diameter plus 0.001 
- This in turn dictated the minimum standard tap diameter - 5/16 
- We want to use standard tap sizes because this drastically reduces difficulty in finding tooling of actually making the part (vs. machining the threads on or acquiring custom tooling) 
- We've typically used 5/16-18, so went with that 
- Outer wall thickness was set by the tap to be major diameter (0.3125") plus 0.05" - 0.365" (I can't add apparently...) 
- The slot heights were set to barely recess the pen tip, slightly over-extend the pen tip, and fully extend the pen tip
- The width was arbitrarily chosen 
- A countersink was put on the slot edgeÂ 
- Angles on slot were chosen for appearance 
- The clip bolts were separated by 0.25" arbitrarily 
- Clip holder was given its shape because it looked nice 

 Tip 

- Tip angle was chosen because it was snubby but still looked good 
- Tip hole set by the ink cartridge 
- Interior angles and diameters also set by the ink cartridge and spring 
- Length stolen from Rotring 600 
- 0.25" of threads kind of arbitrary 

 Clip 

- Thickness guessed 
- Profile eyeballed 

 Bolt Carriage 

- Length set by slot 
- OD set by the ID of the body 
- Threads set by the width of the slot 

 Bolt 

- Shaft set by width of slot 
- Ball made to look pretty 

  

* * *

  

Changes from preliminary design once experimentation began

- Vibration while reducing diameter of body -\> live center 
- 5/16-18 threads don't work! or 5/16-24 -\> 5/16-48 (specialized tooling!) & smaller interior diameter (.243") 
- Drilling out the body tube required janky use of the drill bit -\> acquire longer drill bit 
- 4-40 screws didn't fit on the clip -\> 2-56 
- Using die difficult -\> die holder from Paul 
- Machining the slot with collet means can't countersink slot -\> indexing head 
- Want to remove minimal material when countersinking, but still break edge nicely -\> 60 degree countersink (using combination drill and countersink) 
- Putting holes in clip -\> basic jig
- Threading endcap, wat -\> no endcap (also allows more threads on the clip) 
- Want to stick on manual lathes for alpha -\> using machine screw and sleeve for bolt 
- Stainless is harder to work with -\> aluminum for alpha prototypes (want to figure out the basic design and how to make it first) 
- Tapered tip also protects our body 
- Thinking of doing hex -\> change outer diameter to 3/8" b/c that's what suppliers have
- Clip too much spring strength -\> make long part 25% thinner
- Clip not slide on easily -\> make lip longer and at higher angle
- Bolt could catch on pants -\> rotate it so it is offset by 90 degrees from clip
- No drills for ID -\> tweak dimensions to fit closest size 
- Bolt hard to machine -\> purchase solid rivets and use die to add threads 
- Best size of solid rivets 1/8" -\> move bolt and carriage threading to 5-40 and widen slot in body 
- Machining diagonal clip relief on body difficult -\> use vertical relief 
- Carriage binds up inside body -\> tighter tolerances and rounded edges 
- Wasted space for clip threads -\> shorter body 
- Knurling double-tracking -\> change tip OD to 0.373" 

* * *
**Miscellaneous Notes:**

- For these dimensions, the hex body looks hideous...
- Slot difference -\> 60 degrees (70 too much visually and for hex)
- Using precision ground 3/8" stock saves a ton of time on the body
- Using the Haas machining center produces better results (particularly for the interior) due to greater rigidity

 | 
  

 |

  

