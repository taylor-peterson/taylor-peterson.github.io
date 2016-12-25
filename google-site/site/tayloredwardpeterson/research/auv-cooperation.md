<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>AUV Cooperation</title>
  <style type="text/css">
div.c8 {background-color: transparent; display: block; font-size: medium; font-style: italic; margin-left: auto; margin-right: auto; text-align: justify}
  div.c7 {font-size: medium; width: 425px}
  div.c6 {font-size: medium; margin-left: auto; margin-right: auto; text-align: justify}
  div.c5 {font-size: 80%; font-style: italic; margin-left: auto; margin-right: auto}
  div.c4 {font-size:medium;margin-right:auto;margin-left:auto}
  div.c3 {text-align:justify;font-size:medium}
  div.c2 {font-size: 80%}
  span.c1 {font-size: 80%}
  </style>

</head>

# AUV Cooperation

  

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

 In order to maximize the probability of detecting a shark, the quantity of information obtained, and the quality of said information, it is advantageous to use multiple AUVs.Â 

  

 In our system, when both AUVs are deployed, they share information via an acoustic modem. This information is used to supplement their own sensor inputs for localization purposes and to coordinate motion (to avoid collisions and to ensure varied sensor vantage points).Â 

  

 The below long-exposure shows a pair of AUVs coordinating to circle a set point. 

[![https://docs.google.com/file/d/0B0Jfms0twG8EMm9DRk9ZSDlueVk/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EMm9DRk9ZSDlueVk)](https://docs.google.com/file/d/0B0Jfms0twG8EMm9DRk9ZSDlueVk/edit?usp=drive_web)

 Long exposure of a night mission. The two Ivers are circling about a set location. 

  

 The below animation shows how they do this more explicitly. The data used in the animation was collected during field testing at Catalina Island in the summer of 2012. 

<iframe width="425" height="265" frameborder="0" allowfullscreen="true" src="https://docs.google.com/file/d/0B0Jfms0twG8ENFpxNi0tQkVOUEU/preview">
              </iframe>

  

 Both AUVs are tracking a common circle, then later depart to track a separate circle. To avoid collisions, the two robots are at different radii and leave the circle at different times (note that in the current algorithm, the AUVs depart off the closest point of the circle, rather than the furthest). To ensure varied sensor vantage points, the two AUVs modulate their speed to remain opposite one another.Â 

 Â 

 | 
  

 |

  

