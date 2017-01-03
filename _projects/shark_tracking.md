---
title: Shark Tracking
status: completed
dates: ??
image_path: https://drive.google.com/uc?id=0B0Jfms0twG8EUVhHemJwVFE1VFU
---

# Introduction

I began working with Professor Christopher Clark in the [Lab for Autonomous and
Intelligent Robotics (LAIR)](http://newwww.hmc.edu/lair)in the fall of my
sophomore year as a member of the Shark Tracking team.

The LAIR has over 10 student researchers working on four major projects and
several individual topics. When I joined, the Shark Tracking team consisted of
two other Mudd students (Yukun Lin and Hannah Kastein) and me. Since then,
Richard Piersall and Rowan Zellers have joined the team while Hannah has left.

{% include image.html
id="0B0Jfms0twG8EQUtDS3k0b2x5UHM"
width="615px"
height="410px"
caption="The LAIR team during the summer of 2013. Prof Clark is at the far right."
%}

This project is described briefly on the [LAIR
Projects](http://newwww.hmc.edu/lair/projects.html) page (click on_AUV Shark
Tracking_ on the left hand side). For an idea of where the project stood before
I joined on, check out [this abc7 News
story](http://abclocal.go.com/kabc/story?section=news/local/los_angeles&id=8823629)
about a test-deployment to Catalina Island the summer before I joined on. To
see what was going on in the LAIR in the summer of 2013, check out
this[post](http://newwww.hmc.edu/admission/2013/07/robots/) on the HMC
admissions blog. One of our Catalina field deployments during the summer was
written up by the [Orange County
Register](https://drive.google.com/file/d/0B0Jfms0twG8EQ081X0NtTW5yWm8/edit?usp=sharing).

For an more in-depth description of the project, check out the
[Overview](/research/overview) page.

My main job on the team is improving the control algorithms: we have software
running on the robot telling it where to go to find the sharks - I'm
responsible for making that software smarter and more efficient. In addition to
that, I work to improve the hardware on the robots. For more information on
each of these, check out the software and hardware pages respectively.

One of the awesome things about this project is getting up close and personal
with a lot of sharks. The below video is a compilation of some of the footage
we captured at Catalina Island in the summer of 2013.

<iframe width="425" height="265" frameborder="0" allowfullscreen="true"
src="https://docs.google.com/file/d/0B0Jfms0twG8ENVUzczF4cTlHdmM/preview">
</iframe>

# Overview

The shark tracking project is a cooperative effort between the LAIR and the
[CSU Longbeach Shark Lab](http://www.csulb.edu/labs/sharklab/). Professor Chris
Lowe (I know, another Chris... it gets confusing sometimes), who heads up the
shark lab, is interested in collecting high-resolution positioning data on
sharks and other fish. This data is an important tool for maintaining fish
populations and their habitat. In other words, by figuring out where sharks go
and why, we can better protect them and the marine ecosystem.

[![https://docs.google.com/file/d/0B0Jfms0twG8EczUtY1pCU2RBWFE/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EczUtY1pCU2RBWFE)](https://docs.google.com/file/d/0B0Jfms0twG8EczUtY1pCU2RBWFE/edit?usp=drive_web)

One of the Leopard Sharks we tagged at Catalina Island.

Unfortunately, the current methods of tracking are not sufficient: GPS tracking
tags do not transmit underwater; stationary arrays of sensors only work if the
tagged animal is inside the boundaries of the array; and manual tracking is
labor-intensive and expensive. As such, our team is developing a means of
autonomous active tracking.

The problem we are working on boils down to the following: given position data
for the robot and a set of sensor measurements, determine the position of the
shark.

Now, that might not sound too difficult at first, but let me assure you that it
is. It is very difficult. This difficulty stems from the large number of
variables we are working with and the technological limitations we are trying
to overcome.

We are using two OceanServer Iver2 AUVs. The Iver2 AUV is a torpedo-shaped
robot, that has a rear propeller for propulsion and four fins to control pitch
and yaw. The sensor payload includes a 3-DOF (degree of freedom) compass,
wireless antenna, GPS receiver, and Doppler Velocity Logger.

[![https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EUVhHemJwVFE1VFU)](https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web)

This project uses two OceanServer Iver2 AUVs

The AUVs communicate with each other, as well with a top-side modem, via a
Woods Hole Oceanographic Institution Micro-Modem and externally mounted
transducers. Each AUV is outfitted with a Lotek MAP600RT receiver and an
associated stero-hydrophone set, designed to listen for acoustic signals at a
frequency of 76 kHz.

[![http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/8823616_600x338.jpg](http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/8823616_600x338.jpg)](http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/8823616_600x338.jpg)

Each robot is outfitted with a full sensor payload.

These allow the vehicles to receive transmissions from Lotek MM-M-16-50-PM
acoustic tags, which send a transmission at 76.8 kHz every two seconds.

<figure>
<img src="https://drive.google.com/uc?id=0B0Jfms0twG8EMHl3cXVnRDh5cU0">
<figcaption>
The sharks are tagged with these Lotek tags; the hydrophones on the AUVs are
configured to pick up the acoustic transmissions from the tags.
</figcaption>
</figure>


The Lotek MapHost software associated with the receiver records the tag ID,
time of detection, signal strength, pressure, and presence of motion. This
information and the separation of the hydrophones allows the angle between the
AUV and the acoustic tag to be calculated.

[![](https://drive.google.com/uc?id=0B0Jfms0twG8EWEFucF96V1Y1OHM)](https://docs.google.com/file/d/0B0Jfms0twG8EWEFucF96V1Y1OHM/edit?usp=drive_web)

To localize on a shark, we take readings from a pair of hydrophones (h1 and
h2). From this data, we can calculate the relative angle between the Iver's
heading and the shark's position (alpha). However, there is ambiguity as to
whether the shark is to the right or left of the robot.

There are several challenges associated with state estimation given the sensor
measurements. As indicated above, a shark located at to the left of the robot
will generate the same measurement as one located at the corresponding angle on
the rate. In addition, the stereo-hydrophone system generates an angle-to-tag
measurement with a resolution of approximately 10 degrees. Furthermore, the
rate at which an angle measurement is obtained is highly dependent on the
acoustic environment; time intervals of up to 30 seconds without new
measurements are common. Furthermore, even with distance measurements to the
shark, the actual state of the shark cannot be determined from the signal data
alone.

To determine where the shark actually is, we use something called Monte Carlo
Localization (MCL). In this technique, estimates of the target's location are
represented by a set of "particles". Each particle has an associated weight
that corresponds to how likely it is.

Initially, particle states are assigned randomly within a bounded area centered
on the robot.

[![](https://drive.google.com/uc?id=0B0Jfms0twG8Ecl9IN0FKOUd6QTA)](https://docs.google.com/file/d/0B0Jfms0twG8Ecl9IN0FKOUd6QTA/edit?usp=drive_web)

The position of the shark is initially estimated by a random set of particles.

At each time step afterwards, particles are propagated according to a
stochastic motion model that simulates shark motion.

[![](https://drive.google.com/uc?id=0B0Jfms0twG8ENVhmWk9OMFZLazA)](https://docs.google.com/file/d/0B0Jfms0twG8ENVhmWk9OMFZLazA/edit?usp=drive_web)

The positions are updated at each time step according to a motion model of the
shark.

Afterwards, the weights of the particles are recalculated based on sensor
measurements.

[![](https://drive.google.com/uc?id=0B0Jfms0twG8ESmlMWXktRE1VMzQ)](https://docs.google.com/file/d/0B0Jfms0twG8ESmlMWXktRE1VMzQ/edit?usp=drive_web)

Weights are assigned to each of the particles based on sensor data.

The estimated shark state is then taken to be the average of all estimates. A
new set of particles is then culled from the current set, with preference to
the most probably ones.

At this point, we have an estimated shark position. But what do we do then?
Check out the [Tracking System](/research/tracking-system) and [AUV
Cooperation](/research/auv-cooperation) pages to find out more.

# Software

## Framework

Much of my first few months on the team was spent simply understanding the
code-base and how all of the sub-systems worked and interacted. The
pre-existing control code was especially difficult to understand. Due to the
pressures of debugging in the field and the lack of a pre-existing framework to
work in, the majority of the code ended up being inside the GUI used to set up
missions!

I decided that we needed to set up a framework for the shark tracking code in
order to make it more modular, extensible, and maintainable. My initial plan
was to use something like [ROS](http://www.ros.org/about-ros/) or
[MOOS](http://www.robots.ox.ac.uk/~mobile/MOOS/wiki/pmwiki.php), but neither
worked with Windows (which was required for our system). Furthermore, none of
the other frameworks I could find would work for our use. As such, I chose to
implement a custom framework based on the
[publish-subscribe](http://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern)
principle.

To that end, I divided up our system into two interfaces and five subsystems:

- **User Interface (UI)**: this could take the form of a GUI or a console
application
- **Shark Tracking Interface (STI)**: this serves as an abstraction layer for
all of the shark tracking code and as a broker for implementing
publish-subscribe. This makes it so the UI can't directly access any of the
shark tracking code, which keeps everything modular.
- **Localization** : responsible for figuring out where the shark is relative
to the Iver based on sensor data
- **Controller** : directs the Iver's motion based on its current position, the
position of the other robot, and the estimated position of the shark
- **Database** : stores all sensor and state estimation data along with
relevant control variables. Grouping the data in this way makes it easy to
generate comprehensive and up-to-date log files.
- **Intra-AUV Communications** : each Iver contains two processors. The primary
processor runs proprietary code which interfaces with the sensors and actuators
on the robot. The secondary processor runs our code. This module is responsible
for ensuring that the two processors share relevant data.
- **Inter-AUV Communications** : given that this is a multi-robot system, it is
advantageous to have each robot know what the other is up to

A graphical overview of the interactions between each subsystem can be seen
below. Note that all connections are two-way.

[![](https://drive.google.com/uc?id=0B0Jfms0twG8Ed1U2N2JzRnhMRUk)](https://docs.google.com/file/d/0B0Jfms0twG8Ed1U2N2JzRnhMRUk/edit?usp=drive_web)
Block diagram of the current code layout.

Because each subsystem and the UI only interfaces with the STI, modules can be
readily swapped out. As well, it is easy for team members to work on separate
parts of the code without worrying about stepping on each others' feet.

In all, re-factoring the entire code-base resulted in a much more
comprehensible, robust, and modular system that was far easier to work with
going forward.

## Tracking System

The goal of the tracking system is to localize on a shark and then remain close
to it. At the same time, however, we don't want to alter its behavior, so the
robot should keep its distance. To that end, the system currently uses a
behavior-based controller.

When the robot is close to where it thinks the shark is, it will circle that
point at a safe distance. Once its estimate of the shark's position has moved
appreciably, it will then head directly for that new position and start
circling once it gets close.

[![https://docs.google.com/file/d/0B0Jfms0twG8EMVpwRkJxRjlNcE0/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EMVpwRkJxRjlNcE0)](https://docs.google.com/file/d/0B0Jfms0twG8EMVpwRkJxRjlNcE0/edit?usp=drive_web)

Long exposure of a night mission. The Iver was previously circling a target,
but is now moving to a new target location. [Ben Chasnov]

The robot is currently constrained to a bounded area; it is not allowed to
circle or target a point outside of this boundary. The boundary was set in
order to ensure the robot did not collide with the dock or any of the boats and
so that it avoided the large kelp beds closer to shore (not shown in the
background image). In the future, we hope to incorporate additional sensors to
allow the Iver to avoid obstacles itself, such that the boundary would become
largely unnecessary.

A visualization of a test run (one Iver tracking a tagged boat) is shown below.
This is an excellent example of how the system works because we have truth data
for the positions of the boat and the AUV (both have GPS locators on them). The
meaning of each of the features in the video is as follows:

- As the legend indicates, the red dot is the estimated position of the target
(in this case a boat), the yellow dot is the actual position of the boat, and
the purple dot is the AUV.
- The blue circle around the AUV is the current range estimate to the target.
- The two blue cones emanating from the AUV are the current angular position
estimates to the target. These are calculated using data collected from the
hydrophones by Lotek's proprietary software.
- The dotted green line is the designated operating region of the robot (set in
the code using GPS coordinates for the corners).

<iframe width="425" height="265" frameborder="0" allowfullscreen="true"
src="https://docs.google.com/file/d/0B0Jfms0twG8EMHQxVkxqWU84Rlk/preview"></iframe>

As you can see, the AUV's estimate of the position is quite accurate and
consistent. This is rather remarkable given the poor quality of the data and
low sampling rate (typically we'll get one valid sample every 10-15 seconds,
but one sample per three seconds is the maximum). This localization is Yukun's
focus in the project. For more information on calculating distance and the
localization techniques used, check out our paper from the 2013 UUST
conference: _Using Time of Flight Distance Calculations for Tagged Shark
Localization
[[PDF](http://newwww.hmc.edu/lair/publications/2013/lin_UUST_2013.pdf)]._

As for my controller, you can see that it does remain correctly bounded and
switches its circling point when the target has moved sufficiently.

## AUV Cooperation

In order to maximize the probability of detecting a shark, the quantity of
information obtained, and the quality of said information, it is advantageous
to use multiple AUVs.

In our system, when both AUVs are deployed, they share information via an
acoustic modem. This information is used to supplement their own sensor inputs
for localization purposes and to coordinate motion (to avoid collisions and to
ensure varied sensor vantage points).

The below long-exposure shows a pair of AUVs coordinating to circle a set
point.

[![https://docs.google.com/file/d/0B0Jfms0twG8EMm9DRk9ZSDlueVk/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EMm9DRk9ZSDlueVk)](https://docs.google.com/file/d/0B0Jfms0twG8EMm9DRk9ZSDlueVk/edit?usp=drive_web)

Long exposure of a night mission. The two Ivers are circling about a set
location.

The below animation shows how they do this more explicitly. The data used in
the animation was collected during field testing at Catalina Island in the
summer of 2012.

<iframe width="425" height="265" frameborder="0" allowfullscreen="true"
src="https://docs.google.com/file/d/0B0Jfms0twG8ENFpxNi0tQkVOUEU/preview">
</iframe>

Both AUVs are tracking a common circle, then later depart to track a separate
circle. To avoid collisions, the two robots are at different radii and leave
the circle at different times (note that in the current algorithm, the AUVs
depart off the closest point of the circle, rather than the furthest). To
ensure varied sensor vantage points, the two AUVs modulate their speed to
remain opposite one another.

# Hardware

In addition to working on software, I design and manufacture new hardware.
In particular, I have redesigned the hydrophone mounting hardware and
retrofitted the [kort nozzle](http://en.wikipedia.org/wiki/Ducted_propeller)
and rudder.

Note that pictures of the new system will be added around the third week of
January when I regain access to the lab.

### Hydrophone Mounting Hardware

In order to get useful localization data, the hydrophones must be offset from
the body of the Iver by approximately 0.4 meters and at a spacing of 2.4
meters. The offset from the body of the Iver is to avoid interference from the
propeller and ensure that the sensors remained submerged during surface runs;
the spacing is necessary to get adequate angular resolution.

The old system made use of foam padding and hose clamps to hold a single-piece
PVC frame to the Ivers. The hydrophones and their cables were then taped to the
frame.

{% include image.html
    url="http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/1209est-robot-headon-gwen-goodmanlowe-07.jpg"
    width="551px"
    height="730px"
    caption="In the past, the hydrophones were attached to the AUV using a lot of tape,
             foam, strap clamps, and a single-piece PVC frame."
%}

This system was bulky (both to transport and hydrodynamically), took forever to
set up or tear down, and looked terrible.

I ended up machining mounting brackets to attach the hydrophone frame to the
AUVs' racks. I then mocked up a modular frame out of PVC as a prototype. This
frame was able to break down into a small bundle that was much easier to
transport than the previous frame. To make tape unnecessary, I designed
mounting brackets for the hydrophones and clips to attach the cables to the
frame. To top it all off, Hannah shortened up the cables.

[![https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EUVhHemJwVFE1VFU)](https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web)

The current system uses a modular PVC frame, 3D printed hydrophone holders,
custom-machined mounting hardware, and laser-cut delrin cable holders.

Previously, assembling the frame took close to 15 minutes of fumbling around
and a headache. With the prototype system, it was as simple as threading
together a few parts, sliding the hydrophones in place and tightening them
down, then snapping the cord into the holders. Not only is it a lot easier and
less painful, it's less wasteful too!

One thing that I forgot to consider was that removing all of the foam
previously in the mounting system drastically affected the buoyancy of the
Ivers. The first time we tested out the new mounting system, the Iver sunk!
Fortunately, it was only in a few feet of water, so we didn't lose it. But it
was in Phake Lake in the Bernard Field Station and that water is gross, so I
wasn't too happy about having to dive in after it. Afterwards, we were able to
take out some of the ballast and the Ivers achieved neutral buoyancy once
again.

Unfortunately, the current prototype system is not sufficient for extended use
- while the cord holders are durable enough for continued use, the 3D printed
hydrophone holders and PVC frame have not held up well. Repeatedly tightening
and loosing the screws in the holders eventually causes them to fall apart; the
joints on the PVC frames are not flush, making them a major stress riser that
will fail if the Ivers are transported with the frames attached (the bouncing
motion is too much for the PVC to withstand).

That said, work is in progress to replace the 3D printed parts with machined
ones and the PVC frame with a carbon fiber one.

### Kort Nozzle and Rudder

I also modified the existing rudders in order to be able to attach the long
absent kort nozzles and thereby improve the speed and efficiency of the Ivers.
In order to attach them, I also had to manufacture new support struts for the
nozzles - the old ones were bent out of shape during transport on an earlier
mission.

# Publications

## Recent Work

- Using Time of Flight Distance Calculations for Tagged Shark Localization [[PDF](http://newwww.hmc.edu/lair/publications/2013/lin_UUST_2013.pdf)] (I co-authored this paper)
- Using Time of Flight Distance Calculations for Tagged Shark Localization with an AUV **(I co-authored this paper)**

## Previous Work

- Tracking and Following of a Tagged Leopard Shark with an Autonomous Underwater Vehicle
- A Multi-AUV System for Cooperative Tracking and Following of Leopard Sharks [[PDF](http://newwww.hmc.edu/lair/publications/2013/shinzaki_ICRA_2013.pdf)]
- Tracking of A Tagged Leopard Shark with an AUV: Sensor Calibration and State Estimation [[PDF](http://newwww.hmc.edu/lair/publications/2012/forney_lowe_2012.pdf)]
- Multi-Robot Control for Circumnavigation of Particle Distributions [[PDF](http://newwww.hmc.edu/lair/publications/2012/tang_DARS_2012.pdf)]

# Misc. Photos

[![https://docs.google.com/file/d/0B0Jfms0twG8ETWZObUZIel9RNm8/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8ETWZObUZIel9RNm8)](https://docs.google.com/file/d/0B0Jfms0twG8ETWZObUZIel9RNm8/edit?usp=drive_web)

_Acoustic tags are a key piece of equipment for the Shark Tracking group._ _In order to preserve battery life, each tag must be turned off after use._ _Unfortunately, this is not as simple as flipping a switch - you have to precisely position a magnet on the body of the tag._ _Given that I was the only one on the team capable of hearing the tags, that job fell to me._

[![https://docs.google.com/file/d/0B0Jfms0twG8ERS1Gemw5ZjEzZUk/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8ERS1Gemw5ZjEzZUk)](https://docs.google.com/file/d/0B0Jfms0twG8ERS1Gemw5ZjEzZUk/edit?usp=drive_web)

While cleaning the lab, Sean and I thought to ourselves: "What would be better than an Iver2?"

Our answer: an Iver4.

[![https://docs.google.com/file/d/0B0Jfms0twG8EWkxvelNHZWRzV0E/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EWkxvelNHZWRzV0E)](https://docs.google.com/file/d/0B0Jfms0twG8EWkxvelNHZWRzV0E/edit?usp=drive_web)

The perfectly immaculate lab after Sean and I cleaned it.

(Unfortunately, it didn't stay in this state for very long.)

[![https://docs.google.com/file/d/0B0Jfms0twG8ENHBBV0ljQ2w2ZkU/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8ENHBBV0ljQ2w2ZkU)](https://docs.google.com/file/d/0B0Jfms0twG8ENHBBV0ljQ2w2ZkU/edit?usp=drive_web)

The storage room... in case you were wondering where all the lab things were in the previous picture.
