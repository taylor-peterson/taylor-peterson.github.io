<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>Clip Screw Selection</title>
  <style type="text/css">
img.c12 {display:block;margin-right:auto;margin-left:auto;text-align:center}
  div.c11 {text-align:justify}
  a.c10 {background-color: transparent; text-decoration: underline}
  span.c9 {font-size: 120%}
  h2.c8 {text-align:justify}
  a.c7 {background-color:transparent;font-size:16px;font-weight:normal}
  span.c6 {background-color:transparent;font-size:16px;font-weight:normal}
  div.c5 {color: #666666}
  span.c4 {background-color:transparent}
  a.c3 {background-color:transparent}
  div.c2 {font-family:arial,sans-serif;font-size:13px}
  span.c1 {color: #666666}
  </style>

</head>

# Clip Screw Selection

  

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

## There are two main concerns regarding screws for the clip. The first is functionality (i.e. it needs to keep the clip attached to the pen and not strip out the threads in the pen body). The second is appearance. We ended up selectingÂ [these screws](http://www.mcmaster.com/#92703a203/=q0xugi)Â for the reasons explained below.

## Functionality

When I began this project, I didn't have much intuition for how many threads were required to hold parts together. So I figured I'd do some research and figure out what's what. Checkout theÂ [write-up](https://sites.google.com/site/tayloredwardpeterson/tutorials/bolts)Â of my findings. The gist of that page is that, for low-load applications, you need to use five full threads to develop full strength.Â 

  

Given that the body wall is ~0.075" thick, that would require the use of a #1 screw. That's tiny! The smallest size screw I could reasonably use (without worrying overmuch about breaking taps, etc.) would be a 4-40. But with that size screw, I would only be able to fit three threads. According to my research, that would still retain approximately 80% of full strength, which would seem more than enough, but to be sure I calculated that maximum force that could be applied to the bolt before the threads in the pen body would begin to deform:Â 

  

 ![](http://latex.codecogs.com/gif.latex?%5Cdpi%7B150%7D&space;%5Cbegin%7Balign*%7D&space;%5Ctext%7BN%7D&space;&=&space;%5Ctext%7Bnumber&space;of&space;threads&space;engaged&space;=&space;3&space;threads%7D%5C%5C&space;%5Ctext%7Bp%7D&space;&=&space;%5Ctext%7Bpitch&space;=&space;0.6350&space;mm/thread%7D%5C%5C&space;%5Ctext%7BD%7D&space;&=&space;%5Ctext%7Bmajor&space;thread&space;diameter&space;=&space;2.8448&space;mm%7D%5C%5C&space;%5Csigma_%7By,i%7D&space;&=&space;%5Ctext%7Binternal&space;thread&space;material&space;yield&space;stress&space;=&space;55&space;MPa%7D%5C%5C&space;%5C%5C&space;L_e&space;&=&space;%5Ctext%7Blength&space;of&space;engagement%7D%5C%5C&space;A_s,i&space;&=&space;%5Ctext%7Bthread&space;shear&space;area&space;for&space;internal&space;threads%7D%5C%5C&space;%5Csigma_%7Bs,i%7D&space;&=%5Ctext%7Binternal&space;thread&space;material&space;yield&space;shear&space;stress%7D%5C%5C&space;T_%7Bmax%7D&space;&=&space;%5Ctext%7Btension&space;which&space;will&space;cause&space;internal&space;threads&space;to&space;deform%7D%5C%5C&space;%5C%5C&space;L_e&space;&=&space;Np&space;=&space;1.905%5C&space;%5Ctext%7Bmm%7D&space;%5C%5C&space;A_%7Bs,i%7D&space;&=&space;0.5625%5Cpi&space;(D-0.54127p)L_e&space;=&space;8.42%5C&space;%5Ctext%7Bmm%7D%5E2%5C%5C&space;%5Csigma_%7Bs,i%7D&space;&=&space;0.62%5Csigma_%7By,i%7D&space;=&space;34.1%5C&space;%5Ctext%7BMPa%7D&space;%5C%5C&space;T_%7Bmax%7D&&space;=&space;A_%7Bs,i%7D%5Csigma_%7Bs,i%7D&space;=&space;287.122%5C&space;%5Ctext%7BN%7D&space;%5Cend%7Balign*%7D)
  

In other words, a pair of 4-40 screws should be able to take almost my full body-weight before starting to deform the threads they are in. That seems more than sufficient to me.Â 

  

Note that I can still use the metric model in the above analysis because the UTS thread profile matches that of the ISO metric thread screw [[1](http://en.wikipedia.org/wiki/Unified_Thread_Standard)]. There may be some errors, but they should be negligible. The aluminum maximum yield strength used above was obtainedÂ [here](http://en.wikipedia.org/wiki/6061_aluminium_alloy).Â 

## AppearanceÂ 

From an aesthetics standpoint, only button and flat head screws were acceptable. Further, anything other than torx or hex heads would look tacky.Â 

  

Of the above choices, a countersunk Torx screw was chosen. Countersunk because it tends to look better if you do it right; Torx because that's what I found in the size I needed.Â 

 | 
  

 |

  

