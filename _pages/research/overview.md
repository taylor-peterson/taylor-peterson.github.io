---
layout: default
title: Overview
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

The shark tracking project is a cooperative effort between the LAIR and the [CSU Longbeach Shark Lab](http://www.csulb.edu/labs/sharklab/). Professor Chris Lowe (I know, another Chris... it gets confusing sometimes), who heads up the shark lab, is interested in collecting high-resolution positioning data on sharks and other fish. This data is an important tool for maintaining fish populations and their habitat. In other words, by figuring out where sharks go and why, we can better protect them and the marine ecosystem.

[![https://docs.google.com/file/d/0B0Jfms0twG8EczUtY1pCU2RBWFE/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EczUtY1pCU2RBWFE)](https://docs.google.com/file/d/0B0Jfms0twG8EczUtY1pCU2RBWFE/edit?usp=drive_web)

One of the Leopard Sharks we tagged at Catalina Island.

Unfortunately, the current methods of tracking are not sufficient: GPS tracking tags do not transmit underwater; stationary arrays of sensors only work if the tagged animal is inside the boundaries of the array; and manual tracking is labor-intensive and expensive. As such, our team is developing a means of autonomous active tracking.

The problem we are working on boils down to the following: given position data for the robot and a set of sensor measurements, determine the position of the shark.

Now, that might not sound too difficult at first, but let me assure you that it is. It is very difficult. This difficulty stems from the large number of variables we are working with and the technological limitations we are trying to overcome. 

We are using two OceanServer Iver2 AUVs. The Iver2 AUV is a torpedo-shaped robot, that has a rear propeller for propulsion and four fins to control pitch and yaw. The sensor payload includes a 3-DOF (degree of freedom) compass, wireless antenna, GPS receiver, and Doppler Velocity Logger. 

[![https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EUVhHemJwVFE1VFU)](https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web)

This project uses two OceanServer Iver2 AUVs 

The AUVs communicate with each other, as well with a top-side modem, via a Woods Hole Oceanographic Institution Micro-Modem and externally mounted transducers. Each AUV is outfitted with a Lotek MAP600RT receiver and an associated stero-hydrophone set, designed to listen for acoustic signals at a frequency of 76 kHz.

[![http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/8823616_600x338.jpg](http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/8823616_600x338.jpg)](http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/8823616_600x338.jpg)

Each robot is outfitted with a full sensor payload.

These allow the vehicles to receive transmissions from Lotek MM-M-16-50-PM acoustic tags, which send a transmission at 76.8 kHz every two seconds. 

[![](https://drive.google.com/uc?id=0B0Jfms0twG8EMHl3cXVnRDh5cU0)](https://docs.google.com/file/d/0B0Jfms0twG8EMHl3cXVnRDh5cU0/edit?usp=drive_web)

The sharks are tagged with these Lotek tags; the hydrophones on the AUVs are configured to pick up the acoustic transmissions from the tags. 

The Lotek MapHost software associated with the receiver records the tag ID, time of detection, signal strength, pressure, and presence of motion. This information and the separation of the hydrophones allows the angle between the AUV and the acoustic tag to be calculated. 

[![](https://drive.google.com/uc?id=0B0Jfms0twG8EWEFucF96V1Y1OHM)](https://docs.google.com/file/d/0B0Jfms0twG8EWEFucF96V1Y1OHM/edit?usp=drive_web)

To localize on a shark, we take readings from a pair of hydrophones (h1 and h2). From this data, we can calculate the relative angle between the Iver's heading and the shark's position (alpha). However, there is ambiguity as to whether the shark is to the right or left of the robot. 

There are several challenges associated with state estimation given the sensor measurements. As indicated above, a shark located at to the left of the robot will generate the same measurement as one located at the corresponding angle on the rate. In addition, the stereo-hydrophone system generates an angle-to-tag measurement with a resolution of approximately 10 degrees. Furthermore, the rate at which an angle measurement is obtained is highly dependent on the acoustic environment; time intervals of up to 30 seconds without new measurements are common. Furthermore, even with distance measurements to the shark, the actual state of the shark cannot be determined from the signal data alone. 

To determine where the shark actually is, we use something called Monte Carlo Localization (MCL). In this technique, estimates of the target's location are represented by a set of "particles". Each particle has an associated weight that corresponds to how likely it is. 

Initially, particle states are assigned randomly within a bounded area centered on the robot. 

[![](https://drive.google.com/uc?id=0B0Jfms0twG8Ecl9IN0FKOUd6QTA)](https://docs.google.com/file/d/0B0Jfms0twG8Ecl9IN0FKOUd6QTA/edit?usp=drive_web)

The position of the shark is initially estimated by a random set of particles.

At each time step afterwards, particles are propagated according to a stochastic motion model that simulates shark motion. 

[![](https://drive.google.com/uc?id=0B0Jfms0twG8ENVhmWk9OMFZLazA)](https://docs.google.com/file/d/0B0Jfms0twG8ENVhmWk9OMFZLazA/edit?usp=drive_web)

The positions are updated at each time step according to a motion model of the shark.

Afterwards, the weights of the particles are recalculated based on sensor measurements. 

[![](https://drive.google.com/uc?id=0B0Jfms0twG8ESmlMWXktRE1VMzQ)](https://docs.google.com/file/d/0B0Jfms0twG8ESmlMWXktRE1VMzQ/edit?usp=drive_web)

Weights are assigned to each of the particles based on sensor data.

The estimated shark state is then taken to be the average of all estimates. A new set of particles is then culled from the current set, with preference to the most probably ones.

At this point, we have an estimated shark position. But what do we do then? Check out the [Tracking System](/research/tracking-system) and [AUV Cooperation](/research/auv-cooperation) pages to find out more. 
