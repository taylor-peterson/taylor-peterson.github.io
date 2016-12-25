---
layout: page
title: User Interface
---

[Overview](https://sites.google.com/site/tayloredwardpeterson/projects/filamentwinder)

[User Interface](https://sites.google.com/site/tayloredwardpeterson/projects/filamentwinder/userinterface)

This page details the development of the user interface for the filament winder project. 

For this system, Sean and I could see one of two paradigms working: you could either develop a program on the machine itself, or on a computer and then export a set of commands to the device. Note that reprogramming the microcontroller every time a new layup schedule is desired is highly undesirable and as such, not being considered. 

Of these two options, using a computer seems much more practical. Not only will it allow the user to develop the program wherever they want, but it will allow us much greater programming flexibility. We would have much more computational power available to us, could choose which language to use, and would then be able to incorporate a lot more into the end product (i.e. we could run calculations on the part and estimate its strength). A GUI on the computer would also be much more user friendly than a bunch of DIP switches or a small LED display. In addition, the less we do on the PIC, the easier life will be for us and the more portable (meaning microcontroller-independent) and extensible the system will be. 

However, using this method does add the intermediate steps of exporting, importing, and interpreting files. While the export and interpretation steps should be very easy (save to a flash drive and parse a text file respectively), we do not have any experience reading data off of a flash drive using a PIC microcontroller. 

If USB drive interfacing is easy with the PIC, then we think the GUI would be the way to go. Otherwise, we will reconsider our other options. 

From what we've read, USB interfacing could be "simple." Microchip has a [write-up](http://ww1.microchip.com/downloads/en/AppNotes/01145b.pdf) on how to do it, and [additional hardware](http://electronicdesign.com/dsps/interfacing-usb-flash-drive-pic-microcontroller) exists to handle it that we could interface with. However, since we currently don't have access to the hardware to run tests on, we can't be sure. 

Once we're back at Mudd (we're currently on winter break), we'll test out USB interfacing and move forward with the project.
