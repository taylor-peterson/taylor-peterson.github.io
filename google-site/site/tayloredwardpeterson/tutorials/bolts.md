

---
layout: page
title: Bolts
---

  

| 
  

 | 

## Motivation

 When designing myÂ [pen](https://sites.google.com/site/tayloredwardpeterson/system/errors/NodeNotFound?suri=wuid:gx:6c8aecc18d8d8451), one of the design problems I faced was mounting the clip onto the pen body. I decided early on that I wanted the clip to be removable for greater modularity (and in order to more readily install a replacement, should the clip break ). For this type of connection, I've typically used machine screws. However, the wall of the pen body was rather thin (~0.075") and I wasn't sure if there was enough material for threads. Thinking about this made me realizeÂ that I lacked intuition on optimal thread engagement in bolted joints. Just how much thread engagement do you need?

## Research Results

Christopher Cotner once told me that you need to engage at least 5 full threads. But seeing as I may be mis-remembering or Cotner may have been wrong (the former being more likely), I figured I'd do some research to confirm. A couple of sites ([[1](http://www.engineersedge.com/wwwboard/posts/3626.html)], [[2](http://www.sizes.com/tools/bolts_engagement.htm)])Â I visited cite a length of engagement of 1.5 times the diameter of the screw to be a good rule of thumb. For UNC threads[[3](http://en.wikipedia.org/wiki/Unified_Thread_Standard)], this works out to be 7-8 full threads.Â 

  

Being curious as to where this rule of thumb came from and knowing that most rules of thumb have substantial safety margins built into them, I dug around some more and came across an excellentÂ [write-up](http://www.ajaxfast.com.au/downloads/Technical%20notehowmanythreads.pdf)Â by Ajax Fasteners discussing minimum thread engagement. They conducted a first order analysis based on the guideline that the bolt shank should fail before any threads strip. From the equations in this paper, I calculated that when the bolt and what it is threaded into are the same material, only three threads are needed. But if the bolt is much stronger than the material it is threaded into (e.g. stainless steel into aluminum), many more threads are needed (for the stainless steel-aluminum case, using yield strengths foundÂ [here](http://www.engineeringtoolbox.com/young-modulus-d_417.html), 9-10 full threads are required).Â 

  

In addition to the above first order analysis, Ajax conducted a Finite Element Analysis (FEA) for a generic bolted joint carrying 65% of the yield strength of the bolt, which revealed that only the first five threads carry virtually the entire load (with each thread taking ~ 33%, 27%, 20%, 12%, and 8% respectively). According to the paper, additional threads will only carry load once the first thread plastically deforms.Â 

  

 This can be understood by looking at the situation from a stress-strain standpoint. When a load (stress) is applied to the bolted joint, the threads carrying the load will elongate (experience strain). In the linear elastic region, the first five threads will continue to be able to carry the load on their own even as they elongate. However, once the first thread reaches its yield strength, the load it carries will no longer increase in proportion to the amount it elongates. This characteristic of ductile materials can be seen in the figure below (note that the magnitude of the strain at yield is greatlyÂ exaggerated).Â The remaining force must then be supported by additional threads.Â 

[![https://docs.google.com/file/d/0B0Jfms0twG8Ea0ZjVnowdldEcXM/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8Ea0ZjVnowdldEcXM)](https://docs.google.com/file/d/0B0Jfms0twG8Ea0ZjVnowdldEcXM/edit?usp=drive_web)

_Typical Stress vs. Strain diagram for a ductile material (e.g. Steel)Â_ [[4](http://en.wikipedia.org/wiki/File:Stress_Strain_Ductile_Material.png)]

<sup><br></sup>

## Summary

 It follows from the analyses above that the first five threads will hold virtually the entire load for typical loads, but the full thread count calculated in the first order analysis will be necessary for loads close to the failure point of the threads.Â So it looks like Cotner was right after all!Â 

 | 
  

 |

  

