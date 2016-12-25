<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>Process</title>
  <style type="text/css">
div.c10 {font-weight: bold}
  div.c9 {font-size: 120%; font-weight: bold}
  div.c8 {font-weight: bold; text-align: justify}
  div.c7 {text-align:justify}
  div.c6 {font-size: 120%; font-weight: bold; text-align: justify}
  div.c5 {color: #666666}
  span.c4 {background-color:transparent}
  a.c3 {background-color:transparent}
  div.c2 {font-family:arial,sans-serif;font-size:13px}
  span.c1 {color: #666666}
  </style>

</head>

# Process

  

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

 Body 

  

 Blank 

1. Insert bar stock into manual lathe. 
2. Sand stock with 1000 grit sandpaper to improve surface finish.Â 
3. Part off blank with 0.050" extra.Â Â 
4. Insert blank into manual lathe.Â 
5. Face end and bevel edge. 

 Interior Operations 

1. Insert 7 blanks into soft jaws. Be sure to insert a piece of paper towel between the blanks and the movable jaw to ensure equal clamping force on all pieces.Â 
2. Run parts on machining center.Â 

 Exterior Operations 

1. Deburr hex collet block with a stone (if running multiple parts, it helps to have two collet blocks set up to parallelize work).Â 
2. Set up an combination square such that the perpendicular face is 1.5" from the end of the ruler.Â 
3. Set up a 2-4-6 block in the machining center such that the edge of the block is 2" away from the edge of a zeroed blank.
4. Load blank into collet. Use the combination square to ensure that approximately 1.5" of the part is outside of the collet (anything within ~1/8" is good enough).Â 
5. Insert a loaded collet block into the 4th axis attachment on the machining center. Use the 2" gage block to set the zero.Â 
6. Run parts on the machining center. Note that it helps to use one hand for everything covered in coolant and keep the other dry.Â 

 Finishing Operations 

1. With a clip installed, twirl a L drill bit through the interior. Then clean out anything left with a 0.242 reamer.Â 
2. Soak the part in degreaser and run a pipe cleaner through it. 

* * *

 Tip 

  

 Blank 

1. Insert bar stock (aluminum or brass) into CNC lathe.Â 
2. Setup the lathe and tooling.Â Load up the carriage program (030.PT4 - attached below). Refer to the associated text file (030.txt - also attached) for further details.Â 
3. Run parts! Be sure to check parts to ensure all dimensions are correct. 

 Interior Operations 

1. Properly zero CNC mill on first slot in soft jaws. 
2. Create a quick program to position drill at the center of each part. 
3. Stick undersize gage pins into the soft jaws to prop up the blanks.Â 
4. Insert 7 blanks into soft jaws. Be sure to insert a piece of paper towel between the blanks and the movable jaw to ensure equal clamping force on all pieces. 
5. Drill out the interior of the tips.Â 
6. Flip, resecure, and drill out the tip holes.Â 

 Threading 

1. Insert blanks into a collet on a manual lathe.Â 
2. Run the machine at low speed and add exterior threads using a die holder. 
3. Clean up the threads using a threading tool - you'll want to remove all of the unfinished threads. 

 Knurling 

1. Screw the blank into an arbor.Â 
2. Move the live center into place.Â 
3. Turn the machine on (40 RPM).Â 
4. Move the knurling tool (40 teeth, 0.622" diameter) into place (about halfway off the part, tilted 3-5 degrees to the right of perpendicular).Â 
5. Plunge in quickly to about 0.015" below the surface of the part (from when both rollers make contact with the surface).Â 
6. Once both rollers are engaged, start the autofeed (0.025 IPR).Â 

* * *

 Carriage 

  

 Blank 

1. Insert bar stock (aluminum or brass) into CNC lathe.Â 
2. Setup the lathe and tooling.Â Load up the carriage program (020.PT4 - attached below). Refer to the associated text file (020.txt - also attached) for further details.Â 
3. Run parts! Be sure to check parts to ensure all dimensions are correct. 
4. Once blanks have been machined, you have to clean them up. To do so, secure them in a collet block in a vice. File down the nub left over after parting off with a file. Then use a stone if necessary to clean up the edges.Â 

 Threading 

1. Insert a blank into the vice on CNC mill and locate the center of the part.Â 
2. Attach a vice stop flush against the blank.Â 
3. Add another 9 blanks, each flush to its neighbor. Be sure to place a doubled-over piece of paper towel between the movable vice face and the parts - this will account for any discrepancies in length from the filing step above. Note that you will want to put all of the machined edges against the fixed face of the vice for consistency.Â 
4. Create a quick program to position drill at the center of each part.Â 
5. Center drill, drill, and tap each part.Â 
6. Clean up any and all burrs. Quickly countersinking by hand, then using a needle-nose file and stone usually does the trick fairly well.Â 

* * *

 Bolt 

1. Fit rivet head into a collet secured in a collet block in a vice.Â 
2. Hand-thread 5-40 die onto rivet head. Be sure to keep the die orthogonal to the rivet. Thread a full die's width of threads.Â 

* * *

 Clip 

  

 Blank 

1.   

 Profile 

1.   

 Finishing Operations 

1.   

 | 
  

 |

  

