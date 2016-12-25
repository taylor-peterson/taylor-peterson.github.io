---
layout: default
title: Lessons Learned
---

[Overview](/projects/abetterpen)

[Problem Statement](/projects/abetterpen/problemstatement)

[Preliminary Design](/projects/abetterpen/preliminarydesign)

Component Selection 

    [Ink Cartridge](/projects/abetterpen/cartridgeselection)

    [Clip Screw](/projects/abetterpen/clipscrewselection)

[Prototyping](/projects/abetterpen/alphaprototype)

"Mass" Production 

   Bill of Materials 

   [Process](/projects/abetterpen/process)

   Drawings/Parts 

   [Lessons Learned](/projects/abetterpen/lessonslearned)

Body

Doing the 4th axis work before the internal work probably would have cut down on the number of burrs. Might also have resulted in problems with chip removal though. 

**Knurling**

Knurling works best when the decimal component of the value given by TxD<sub>p</sub>/D<sub>r</sub> is within 0.15 of 0. Note that T is the number of teeth on the roller, D<sub>p</sub> is the diameter of the part, and D<sub>r</sub> is the diameter of the roller. 

If we had access to a CNC machine that could knurl, we would have done the knurling operation before adding the taper to the tip. This is because the first 1/4" of knurls are usually not very pretty, so changing the order of operations would allow us to cut that part off. 

Carriages

Deburring the threaded hole on the carriages was time-consuming (particularly for the aluminum). This could have been alleviated by adding a dip in the profile of the carriage. Doing so would recess the threaded hole and obviate this problem. 

Clip

If we were to make more pens in the future, we would probably make the clips using a forming process as doing so would greatly reduce the time per part. 

G-2 Inserts

The grey-tipped G-2 inserts have slightly larger geometry than the blue-tipped ones. We were able to accommodate this by filing down the OD of the tip of the grey-tipped inserts. 

Tip

For some reason, we had difficulties drilling the tip hole in the center of the part. 

Material Choice

Brass is much more difficult to machine than aluminum, but looks much nicer as a carriage. In addition, the brass tended to flake off instead of producing large chips which meant it was much simpler to deburr. 
