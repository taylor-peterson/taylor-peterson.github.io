<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>Tracking System</title>
  <style type="text/css">
div.c12 {text-align:center}
  i.c11 {background-color:transparent}
  div.c10 {text-align:center;font-style:italic}
  div.c9 {font-style: italic; width: 425px}
  li.c8 {text-align:justify}
  span.c7 {background-color:transparent}
  span.c6 {font-size:medium;background-color:transparent}
  div.c5 {font-size: 80%; font-style: italic; text-align: center}
  div.c4 {display: block; margin-left: auto; margin-right: auto; text-align: center}
  div.c3 {text-align:justify}
  div.c2 {font-size: 80%}
  span.c1 {font-size: 80%}
  </style>

</head>

# Tracking System

  

| 

  

[Introduction](https://sites.google.com/site/tayloredwardpeterson/research)

  

[Overview](https://sites.google.com/site/tayloredwardpeterson/research/overview)

  

 Software 

 Â Â Â [Framework](https://sites.google.com/site/tayloredwardpeterson/research/software)  

 Â Â Â [Tracking System](https://sites.google.com/site/tayloredwardpeterson/research/tracking-system)  

Â Â Â [AUV Cooperation](https://sites.google.com/site/tayloredwardpeterson/research/auv-cooperation)  

  

[Hardware](https://sites.google.com/site/tayloredwardpeterson/research/hardware)

  

[Field Testing](https://sites.google.com/site/tayloredwardpeterson/research/field-testing)

  

[Publications](https://sites.google.com/site/tayloredwardpeterson/research/publications)

  

[Misc. Photos](https://sites.google.com/site/tayloredwardpeterson/research/misc)

  

 | 

 The goal of the tracking system is to localize on a shark and then remain close to it. At the same time, however, we don't want to alter its behavior, so the robot should keep its distance. To that end, the system currently uses a behavior-based controller.Â 

  

 When the robot is close to where it thinks the shark is, it will circle that point at a safe distance. Once its estimate of the shark's position has moved appreciably, it will then head directly for that new position and start circling once it gets close. 

  

[![https://docs.google.com/file/d/0B0Jfms0twG8EMVpwRkJxRjlNcE0/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EMVpwRkJxRjlNcE0)](https://docs.google.com/file/d/0B0Jfms0twG8EMVpwRkJxRjlNcE0/edit?usp=drive_web)

 Long exposure of a night mission. The Iver was previously circling a target, but is now moving to a new target location. [Ben Chasnov] 

  

The robot is currently constrained to a bounded area; itÂ is not allowed to circle or target a point outside of this boundary. The boundary was set in order to ensure the robot did not collide with the dock or any of the boats and so that it avoided the large kelp beds closer to shore (not shown in the background image). In the future, we hope to incorporate additional sensors to allow the Iver to avoid obstacles itself, such that the boundary would become largelyÂ unnecessary.Â 

  

A visualization of a test run (one Iver tracking a tagged boat) is shown below. This is an excellent example of how the system works because we have truth data for the positions of the boat and the AUV (both have GPS locators on them). The meaning of each of the features in the video is as follows:

- As the legend indicates, the red dot is the estimated position of the target (in this case a boat), the yellow dot is the actual position of the boat, and the purple dot is the AUV.Â 
- The blue circle around the AUV is the current range estimate to the target.Â 
- The two blue conesÂ emanating from the AUV are the current angular position estimates to the target. These are calculated using data collected from the hydrophones by Lotek's proprietary software.Â Â 
- The dotted green line is the designated operating region of the robot (set in the code using GPS coordinates for the corners).Â 

<iframe width="425" height="265" frameborder="0" allowfullscreen="true" src="https://docs.google.com/file/d/0B0Jfms0twG8EMHQxVkxqWU84Rlk/preview"></iframe>

  

As you can see, the AUV's estimate of the position is quite accurate and consistent. This is rather remarkable given the poor quality of the data and low sampling rate (typically we'll get one valid sample every 10-15 seconds, but one sample per three seconds is the maximum). This localization is Yukun's focus in the project. For more information on calculating distance and the localization techniques used, check out our paper from the 2013 UUST conference:Â _Using Time of Flight Distance Calculations for Tagged Shark Localization [[PDF](http://newwww.hmc.edu/lair/publications/2013/lin_UUST_2013.pdf)].Â_ 

  

As for my controller, you can see that it does remain correctly bounded and switches its circling point when the target has moved sufficiently.

 | 
  

 |

  

