---
layout: page
title: Framework
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

Much of my first few months on the team was spent simply understanding the code-base and how all of the sub-systems worked and interacted. The pre-existing control code was especially difficult to understand. Due to the pressures of debugging in the field and the lack of a pre-existing framework to work in, the majority of the code ended up being inside the GUI used to set up missions! 

I decided that we needed to set up a framework for the shark tracking code in order to make it more modular, extensible, and maintainable. My initial plan was to use something like [ROS](http://www.ros.org/about-ros/) or [MOOS](http://www.robots.ox.ac.uk/~mobile/MOOS/wiki/pmwiki.php), but neither worked with Windows (which was required for our system). Furthermore, none of the other frameworks I could find would work for our use. As such, I chose to implement a custom framework based on the [publish-subscribe](http://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern) principle. 

To that end, I divided up our system into two interfaces and five subsystems: 

- **User Interface (UI)**: this could take the form of a GUI or a console application
- **Shark Tracking Interface (STI)**: this serves as an abstraction layer for all of the shark tracking code and as a broker for implementing publish-subscribe. This makes it so the UI can't directly access any of the shark tracking code, which keeps everything modular.
- **Localization** : responsible for figuring out where the shark is relative to the Iver based on sensor data
- **Controller** : directs the Iver's motion based on its current position, the position of the other robot, and the estimated position of the shark
- **Database** : stores all sensor and state estimation data along with relevant control variables. Grouping the data in this way makes it easy to generate comprehensive and up-to-date log files. 
- **Intra-AUV Communications** : each Iver contains two processors. The primary processor runs proprietary code which interfaces with the sensors and actuators on the robot. The secondary processor runs our code. This module is responsible for ensuring that the two processors share relevant data.
- **Inter-AUV Communications** : given that this is a multi-robot system, it is advantageous to have each robot know what the other is up to

A graphical overview of the interactions between each subsystem can be seen below. Note that all connections are two-way. 

[![](https://drive.google.com/uc?id=0B0Jfms0twG8Ed1U2N2JzRnhMRUk)](https://docs.google.com/file/d/0B0Jfms0twG8Ed1U2N2JzRnhMRUk/edit?usp=drive_web)
Block diagram of the current code layout.

Because each subsystem and the UI only interfaces with the STI, modules can be readily swapped out. As well, it is easy for team members to work on separate parts of the code without worrying about stepping on each others' feet. 

In all, re-factoring the entire code-base resulted in a much more comprehensible, robust, and modular system that was far easier to work with going forward. 
