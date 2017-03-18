---
title: A Better Pen
summary: Such shiny
start_date: [2013,12,23]
end_date: [2015,05]
image_path: projects/abetterpen/betterPenPrototype.png
---

# Overview

I'm a self-professed pen and pencil snob. I strongly prefer extremely fine tips
(~0.4 mm) and high quality, all-metal construction. In the mechanical pencil
realm, there are some commercial offerings that have appeased me for the time
being (namely, the Rotring 600). Unfortunately, there doesn't appear to be a
pen equivalent to these. While there are a number of cartridges in the 0.4 mm
size range that work quite well, most come encased in plastic bodies and none
of the metal-bodied ones are suitable. Fortunately for me, making a all-metal
pen body is within my reach.


# Problem Statement

## Background

Personally, I do not like having caps on my pens (too easy to lose, two hand
operation, etc.) and as such want a retractable pen. That said, traditional
"clicky" pens annoy me with their noise. The only way I could think of making a
quiet retractable pen (that could still be worked with one hand) was with a
"bolt action" mechanism. Turns out that this design has been up and coming with
the Kickstarter crowd and several versions have been made previously. For
example, the
[TiBolt](http://jumpstartcity.com/events/tibolt-the-american-made-titanium-bolt-action-pen/c),
[The
Bolt](http://fromthepencup.wordpress.com/2013/03/19/the-bolt-a-machined-bolt-action-pen/),
and the [maxmadco retractable
pen](http://maxmadco.com/products/retractable-pen/).

However, all of these are rather expensive (\>$50) and might not be work well
with the cartridges I prefer. As well, I am not a fan of certain
characteristics of each: the TiBolt's finish looks too rough and the pen itself
seems a little bulky (see
[this](http://edcforums.com/threads/the-tibolt-compared-to-the-embassy-pen-and-now-the-madmaxco.105871/)comparison
of it to the maxmadco); the Bolt's mechanism seems like it would be finicky/not
very satisfying; the bolt on the maxmadco looks a little tacky given that it's
just a screw.

Given those concerns, I think it would be preferable to design my own pen. Of
the three, I like the maxmadco one the best (I'd probably buy it and replace
the bolt with something similar to the TiBolt if it cost about a third of what
it did).

## Design Requirements

- All components save the ink cartridge _must_ be made of metal
- The pen _must_ have a retractable design
- The pen _must_ have a functional clip
- The ink cartridge _must_ be replaceable
- All components _must_ be manufacturable using HMC facilities

- The pen _should_ be approximately 5 inches in length
- The pen _should_ weigh approximately 1.5 ounces
- The user of the pen _should_ be awestruck


# Preliminary Design

After looking at existing pens, I came up with a list of major design decisions to be made:

- Stainless Steel vs. Aluminum
- Tapered vs. Drafting-style tip (by drafting-style I mean like the [Rotring 600](http://cdn.coloradopen.com/images/uploads/rotring-600-pencil-POP.png) or like [these pens](http://coolmaterial.com/gear/apollo-technical-pen-and-drafting-scale/))
- Cylindrical vs. Hexagonal body
- Single vs. multi-piece body
- Replaceable vs. sealed end
- Knurled vs. smooth grip

I currently prefer the first of each set. The reasons for this are as follows:

- I have a big chunk of stainless which could be heat-treated to gold should we desire. As such, I could do silver or gold whereas with aluminum I could only have silver (realistically, I'm not going to pay for anodizing). Although aluminum would be easier to machine.
- The drafting-style tip does increase visibility to the page, but I think the tapered tip looks better overall and that visibility shouldn't be an issue.
- While I do like the hexagonal body of the Rotring pencils, a hexagonal body would require additional machining operations (aka more time) and a change in body geometry between the shaft and grip area (which might not look the best).
- I initially thought of having the body be a single piece with a slot at the top to allow the bolt to slide out and the cartridge to be replaced. However, I think that that design would allow for the bolt to be lost and would complicate fabrication.
- Although I don't anticipate needing a stylus nub or anything similar anytime soon, it wouldn't too much more work to give us that option.
- While the smooth grip might look sleeker, I think the extra grip of a knurled grip would be appreciated.

In summary, I'm thinking of a pen with the following component breakdown:

- Bolt and bolt carriage similar to the [TiBolt](http://jumpstartcity.com/events/tibolt-the-american-made-titanium-bolt-action-pen/c)
- Clip and clip screws similar to any of the above
- Body similar to the [maxmadco](http://maxmadco.com/products/retractable-pen/), but with knurling on the grip and a replaceable tip like the TiBolt as opposed to unscrewing at the middle.
- Replaceable end like on the TiBolt but with the bevel like on the maxmadco.

As I move on to the detailed design stage, these decisions may be changed.

# Component Selection

## Ink Cartridge Selection

Before starting this project, I knew that I wanted a pen nib smaller than 0.5
mm. Anything 0.5 mm or larger is too large (especially when you are trying to
put subscripts on subscripts). However, I didn't know how much smaller I wanted
to go or which refill worked best for me. To that end, I went to the Internet
for advice. The majority of pen users (especially pen fanatics) prefer larger
nibs (usually because they write smoother). There were a few pen forums ([The
Pen Addict](http://penaddict.com/), [Gourmet
Pens](http://www.gourmetpens.com/), and [No Pen
Intended](http://nopenintended.wordpress.com/)) which advocated pens with
smaller nibs, but they were not as definitive as I would have liked. So off to
[JetPens](http://www.jetpens.com/)I went.

I started off by looking for every pen with a nib smaller than 0.5 mm and
readily available refills, focusing exclusively on black (non-erasable) ink.
The first round of pens I got were:

- [Ohto Needle-Point Slim Line 03 Ballpoint Pen (0.3
mm)](http://www.jetpens.com/Ohto-Needle-Point-Slim-Line-03-Ballpoint-Pen-0.3-mm-Black-Body/pd/6728)
- [Uni Jetstream Standard Ballpoint Pen (0.38
mm)](http://www.jetpens.com/Uni-Jetstream-Standard-Ballpoint-Pen-0.38-mm-Black-Ink-Black-Body/pd/10591)
- [Pentel Slicci Gel Ink Pen (0.25
mm)](http://www.jetpens.com/Pentel-Slicci-Gel-Ink-Pen-0.25-mm-Black-Ink/pd/1267)
- [Uni-ball Signo UM-151 Gel Ink Pen (0.28
mm)](http://www.jetpens.com/Uni-ball-Signo-UM-151-Gel-Ink-Pen-0.28-mm-Black/pd/295)

Unfortunately, the Ohto and Jetstream turned out to be too scratchy for my
taste. In addition, ink cartridges in pens with caps (the Signo and Slicci)
generally cannot be placed inside a pen with a bolt action mechanism. The
reason for this is two-fold. First, a pen with this style mechanism requires a
spring, and these cartridges have nowhere to rest such a spring. Secondly, when
actuating the mechanism, the tip has to be pushed further out than its final
location, which requires a long, slim leading section, which these cartridges
also lack.

With this in mind, I made another trip to JetPens and came up with one more
order:

- Zebra Sarasa Push Clip Gel Ink Pen ([0.3
mm](http://www.jetpens.com/Zebra-Sarasa-Push-Clip-Gel-Ink-Pen-0.3-mm-Black/pd/6365)
and [0.4
mm](http://www.jetpens.com/Zebra-Sarasa-Push-Clip-Gel-Ink-Pen-0.4-mm-Black/pd/797))
- Pilot Hi-Tec-C Slim Knock Gel Ink Pen ([0.3
mm](http://www.jetpens.com/Pilot-Hi-Tec-C-Slim-Knock-Gel-Ink-Pen-0.3-mm-Black/pd/1331)
and [0.4
mm](http://www.jetpens.com/Pilot-Hi-Tec-C-Slim-Knock-Gel-Ink-Pen-0.4-mm-Black/pd/2460))
- [Uni-Ball Signo RT UM-138 Gel Ink Pen (0.38
mm)](http://www.jetpens.com/Uni-ball-Signo-RT-UM-138-Gel-Ink-Pen-0.38-mm-Black/pd/466)
- [Pilot G-2 Gel Ink Pen (0.38
mm)](http://www.jetpens.com/Pilot-G-2-Gel-Ink-Pen-0.38-mm-Black/pd/268)
- [Pilot Juice Gel Ink Pen (0.38
mm)](http://www.jetpens.com/Pilot-Juice-Gel-Ink-Pen-0.38-mm-Black/pd/10687)

When testing the new batch of pens, the Hi-Tec-C blew everything else away. It
was just so smooth and precise. The only problem with it is that its refill is
tiny. And I mean really tiny! The below image shows it below a standard G-2
style cartridge.

[![https://docs.google.com/file/d/0B0Jfms0twG8EcHU2VVQzVzhYVDA/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EcHU2VVQzVzhYVDA)](https://docs.google.com/file/d/0B0Jfms0twG8EcHU2VVQzVzhYVDA/edit?usp=drive_web)

Sarasa cartridge (top) vs. Hi-Tec-C Slim Knock cartridge (bottom)

It turns out that there are three other (potentially suitable) refills
available for capped versions of the Hi-Tec-C.

The first is the generic Hi-Tec-C cartridge. As you can see below, it has an
incompatible tip design.

[![https://docs.google.com/file/d/0B0Jfms0twG8EYjZJVVhFallibjg/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EYjZJVVhFallibjg)](https://docs.google.com/file/d/0B0Jfms0twG8EYjZJVVhFallibjg/edit?usp=drive_web)

Profile of the generic Hi-Tec-C cartridge
[[CW&T](http://shop.cwandt.com/products/0-3mm-black-hi-tec-c-gel-ink-refill-bls-hc3)]

The second is a multi-pen cartridge. This one has an incompatible body style.
Moreover, there doesn't appear to be any more ink in one of these cartridges as
compared to the Slim Knock cartridge (and these cartridges cost almost three
times as much!).

[![https://docs.google.com/file/d/0B0Jfms0twG8EeEJ0SUNEaG9kX1E/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EeEJ0SUNEaG9kX1E)](https://docs.google.com/file/d/0B0Jfms0twG8EeEJ0SUNEaG9kX1E/edit?usp=drive_web)

Multi-pen style
[[JetPen](http://www.jetpens.com/blog/pen-mod-hi-tec-c-and-platinum-double-r3-action-multi-pen-modification-tutorial/pt/337)]

The third style is for the high-end version of the Hi-Tec-C, the Cavalier.
Unlike the others, this appears to have a compatible tip and body design. The
below image compares the Cavalier refill to the Zebra Sarasa refill, which I
know I can work with.

[![http://dowdyism.typepad.com/.a/6a0105355ba1e3970c015432927f86970c-pi](http://dowdyism.typepad.com/.a/6a0105355ba1e3970c015432927f86970c-pi)](http://dowdyism.typepad.com/.a/6a0105355ba1e3970c015432927f86970c-pi)

Zebra Sarasa refill top; Cavalier refill bottom. [[Pen
Addict](http://penaddict.com/blog/2011/5/27/pen-hack-zebra-sarasa-clip-to-pilot-hi-tec-c-cavalier.html)]

Cue JetPens order #3!

As for the other pens, the Pilot Juice turned out to be a duplicate of the G2,
the Signo was scratchy, and the Sarasas not quite as smooth and precise as the
G2.

The third batch of pens turned out to be a disappointment. The Cavalier
catridges turned out to be too messy and inconsistent - they tend to get ink
balls and be slow to start after a day or two of no use. While they were
phenomenal when they worked, they just can't match the consistency of the G2.

So in the end, the G2 0.38 wins.

## Clip Screw Selection

There are two main concerns regarding screws for the clip. The first is
functionality (i.e. it needs to keep the clip attached to the pen and not strip
out the threads in the pen body). The second is appearance. We ended up
selecting [these screws](http://www.mcmaster.com/#92703a203/=q0xugi) for the
reasons explained below.

### Functionality

When I began this project, I didn't have much intuition for how many threads
were required to hold parts together. So I figured I'd do some research and
figure out what's what. Checkout the [write-up](/tutorials/bolts) of my
findings. The gist of that page is that, for low-load applications, you need to
use five full threads to develop full strength.

Given that the body wall is ~0.075" thick, that would require the use of a #1
screw. That's tiny! The smallest size screw I could reasonably use (without
worrying overmuch about breaking taps, etc.) would be a 4-40. But with that
size screw, I would only be able to fit three threads. According to my
research, that would still retain approximately 80% of full strength, which
would seem more than enough, but to be sure I calculated that maximum force
that could be applied to the bolt before the threads in the pen body would
begin to deform:

![](http://latex.codecogs.com/gif.latex?%5Cdpi%7B150%7D&space;%5Cbegin%7Balign*%7D&space;%5Ctext%7BN%7D&space;&=&space;%5Ctext%7Bnumber&space;of&space;threads&space;engaged&space;=&space;3&space;threads%7D%5C%5C&space;%5Ctext%7Bp%7D&space;&=&space;%5Ctext%7Bpitch&space;=&space;0.6350&space;mm/thread%7D%5C%5C&space;%5Ctext%7BD%7D&space;&=&space;%5Ctext%7Bmajor&space;thread&space;diameter&space;=&space;2.8448&space;mm%7D%5C%5C&space;%5Csigma_%7By,i%7D&space;&=&space;%5Ctext%7Binternal&space;thread&space;material&space;yield&space;stress&space;=&space;55&space;MPa%7D%5C%5C&space;%5C%5C&space;L_e&space;&=&space;%5Ctext%7Blength&space;of&space;engagement%7D%5C%5C&space;A_s,i&space;&=&space;%5Ctext%7Bthread&space;shear&space;area&space;for&space;internal&space;threads%7D%5C%5C&space;%5Csigma_%7Bs,i%7D&space;&=%5Ctext%7Binternal&space;thread&space;material&space;yield&space;shear&space;stress%7D%5C%5C&space;T_%7Bmax%7D&space;&=&space;%5Ctext%7Btension&space;which&space;will&space;cause&space;internal&space;threads&space;to&space;deform%7D%5C%5C&space;%5C%5C&space;L_e&space;&=&space;Np&space;=&space;1.905%5C&space;%5Ctext%7Bmm%7D&space;%5C%5C&space;A_%7Bs,i%7D&space;&=&space;0.5625%5Cpi&space;(D-0.54127p)L_e&space;=&space;8.42%5C&space;%5Ctext%7Bmm%7D%5E2%5C%5C&space;%5Csigma_%7Bs,i%7D&space;&=&space;0.62%5Csigma_%7By,i%7D&space;=&space;34.1%5C&space;%5Ctext%7BMPa%7D&space;%5C%5C&space;T_%7Bmax%7D&&space;=&space;A_%7Bs,i%7D%5Csigma_%7Bs,i%7D&space;=&space;287.122%5C&space;%5Ctext%7BN%7D&space;%5Cend%7Balign*%7D)

In other words, a pair of 4-40 screws should be able to take almost my full
body-weight before starting to deform the threads they are in. That seems more
than sufficient to me.

Note that I can still use the metric model in the above analysis because the
UTS thread profile matches that of the ISO metric thread screw
[[1](http://en.wikipedia.org/wiki/Unified_Thread_Standard)]. There may be some
errors, but they should be negligible. The aluminum maximum yield strength used
above was obtained [here](http://en.wikipedia.org/wiki/6061_aluminium_alloy).

### Appearance

From an aesthetics standpoint, only button and flat head screws were
acceptable. Further, anything other than torx or hex heads would look tacky.

Of the above choices, a countersunk Torx screw was chosen. Countersunk because
it tends to look better if you do it right; Torx because that's what I found in
the size I needed.

# Prototyping

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
- A countersink was put on the slot edge
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


# Process

Body

Blank

1. Insert bar stock into manual lathe.
2. Sand stock with 1000 grit sandpaper to improve surface finish.
3. Part off blank with 0.050" extra.
4. Insert blank into manual lathe.
5. Face end and bevel edge.

Interior Operations

1. Insert 7 blanks into soft jaws. Be sure to insert a piece of paper towel
   between the blanks and the movable jaw to ensure equal clamping force on all
   pieces.
2. Run parts on machining center.

Exterior Operations

1. Deburr hex collet block with a stone (if running multiple parts, it helps to
   have two collet blocks set up to parallelize work).
2. Set up an combination square such that the perpendicular face is 1.5" from
   the end of the ruler.
3. Set up a 2-4-6 block in the machining center such that the edge of the block
   is 2" away from the edge of a zeroed blank.
4. Load blank into collet. Use the combination square to ensure that
   approximately 1.5" of the part is outside of the collet (anything within
   ~1/8" is good enough).
5. Insert a loaded collet block into the 4th axis attachment on the machining
   center. Use the 2" gage block to set the zero.
6. Run parts on the machining center. Note that it helps to use one hand for
   everything covered in coolant and keep the other dry.

Finishing Operations

1. With a clip installed, twirl a L drill bit through the interior. Then clean
   out anything left with a 0.242 reamer.
2. Soak the part in degreaser and run a pipe cleaner through it.

* * *

Tip

Blank

1. Insert bar stock (aluminum or brass) into CNC lathe.
2. Setup the lathe and tooling. Load up the carriage program (030.PT4 -
attached below). Refer to the associated text file (030.txt - also attached)
for further details.
3. Run parts! Be sure to check parts to ensure all dimensions are correct.

Interior Operations

1. Properly zero CNC mill on first slot in soft jaws.
2. Create a quick program to position drill at the center of each part.
3. Stick undersize gage pins into the soft jaws to prop up the blanks.
4. Insert 7 blanks into soft jaws. Be sure to insert a piece of paper towel
between the blanks and the movable jaw to ensure equal clamping force on all
pieces.
5. Drill out the interior of the tips.
6. Flip, resecure, and drill out the tip holes.

Threading

1. Insert blanks into a collet on a manual lathe.
2. Run the machine at low speed and add exterior threads using a die holder.
3. Clean up the threads using a threading tool - you'll want to remove all of
the unfinished threads.

Knurling

1. Screw the blank into an arbor.
2. Move the live center into place.
3. Turn the machine on (40 RPM).
4. Move the knurling tool (40 teeth, 0.622" diameter) into place (about halfway
off the part, tilted 3-5 degrees to the right of perpendicular).
5. Plunge in quickly to about 0.015" below the surface of the part (from when
both rollers make contact with the surface).
6. Once both rollers are engaged, start the autofeed (0.025 IPR).

* * *

Carriage

Blank

1. Insert bar stock (aluminum or brass) into CNC lathe.
2. Setup the lathe and tooling. Load up the carriage program (020.PT4 -
attached below). Refer to the associated text file (020.txt - also attached)
for further details.
3. Run parts! Be sure to check parts to ensure all dimensions are correct.
4. Once blanks have been machined, you have to clean them up. To do so, secure
them in a collet block in a vice. File down the nub left over after parting off
with a file. Then use a stone if necessary to clean up the edges.

Threading

1. Insert a blank into the vice on CNC mill and locate the center of the part.
2. Attach a vice stop flush against the blank.
3. Add another 9 blanks, each flush to its neighbor. Be sure to place a
doubled-over piece of paper towel between the movable vice face and the parts -
this will account for any discrepancies in length from the filing step above.
Note that you will want to put all of the machined edges against the fixed face
of the vice for consistency.
4. Create a quick program to position drill at the center of each part.
5. Center drill, drill, and tap each part.
6. Clean up any and all burrs. Quickly countersinking by hand, then using a
needle-nose file and stone usually does the trick fairly well.

* * *

Bolt

1. Fit rivet head into a collet secured in a collet block in a vice.
2. Hand-thread 5-40 die onto rivet head. Be sure to keep the die orthogonal to
the rivet. Thread a full die's width of threads.

* * *

Clip

Blank

1.

Profile

1.

Finishing Operations

1.


# Lessons Learned

Body

Doing the 4th axis work before the internal work probably would have cut down
on the number of burrs. Might also have resulted in problems with chip removal
though.

**Knurling**

Knurling works best when the decimal component of the value given by
TxD<sub>p</sub>/D<sub>r</sub> is within 0.15 of 0. Note that T is the number of
teeth on the roller, D<sub>p</sub> is the diameter of the part, and
D<sub>r</sub> is the diameter of the roller.

If we had access to a CNC machine that could knurl, we would have done the
knurling operation before adding the taper to the tip. This is because the
first 1/4" of knurls are usually not very pretty, so changing the order of
operations would allow us to cut that part off.

Carriages

Deburring the threaded hole on the carriages was time-consuming (particularly
for the aluminum). This could have been alleviated by adding a dip in the
profile of the carriage. Doing so would recess the threaded hole and obviate
this problem.

Clip

If we were to make more pens in the future, we would probably make the clips
using a forming process as doing so would greatly reduce the time per part.

G-2 Inserts

The grey-tipped G-2 inserts have slightly larger geometry than the blue-tipped
ones. We were able to accommodate this by filing down the OD of the tip of the
grey-tipped inserts.

Tip

For some reason, we had difficulties drilling the tip hole in the center of the
part.

Material Choice

Brass is much more difficult to machine than aluminum, but looks much nicer as
a carriage. In addition, the brass tended to flake off instead of producing
large chips which meant it was much simpler to deburr.
