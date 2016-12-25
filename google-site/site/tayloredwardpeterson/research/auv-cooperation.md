---
layout: default
title: AUV Cooperation
---

[Introduction](/research)

[Overview](/research/overview)

Software 

    [Framework](/research/software)  

    [Tracking System](/research/tracking-system)  

   [AUV Cooperation](/research/auv-cooperation)  

[Hardware](/research/hardware)

[Field Testing](/research/field-testing)

[Publications](/research/publications)

[Misc. Photos](/research/misc)

In order to maximize the probability of detecting a shark, the quantity of information obtained, and the quality of said information, it is advantageous to use multiple AUVs. 

In our system, when both AUVs are deployed, they share information via an acoustic modem. This information is used to supplement their own sensor inputs for localization purposes and to coordinate motion (to avoid collisions and to ensure varied sensor vantage points). 

The below long-exposure shows a pair of AUVs coordinating to circle a set point. 

[![https://docs.google.com/file/d/0B0Jfms0twG8EMm9DRk9ZSDlueVk/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EMm9DRk9ZSDlueVk)](https://docs.google.com/file/d/0B0Jfms0twG8EMm9DRk9ZSDlueVk/edit?usp=drive_web)

Long exposure of a night mission. The two Ivers are circling about a set location. 

The below animation shows how they do this more explicitly. The data used in the animation was collected during field testing at Catalina Island in the summer of 2012. 

<iframe width="425" height="265" frameborder="0" allowfullscreen="true" src="https://docs.google.com/file/d/0B0Jfms0twG8ENFpxNi0tQkVOUEU/preview">
              </iframe>

Both AUVs are tracking a common circle, then later depart to track a separate circle. To avoid collisions, the two robots are at different radii and leave the circle at different times (note that in the current algorithm, the AUVs depart off the closest point of the circle, rather than the furthest). To ensure varied sensor vantage points, the two AUVs modulate their speed to remain opposite one another. 
