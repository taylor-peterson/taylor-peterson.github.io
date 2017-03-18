---
title: Filament Winder
status: deferred
dates: 2013/11/06-2013/11/27
image_path: filamentWinder.png
---

# Reason for Abandoning

- Cost (time and equipment) to do it right is too high
- I will not actually use the filament winder for anything now that I've dropped the bike project
- I'd be better off spending that time/effort on other things

# Progress

- Work on a motor controller for the mandrel, as documented on Sean's site [here](https://sites.google.com/site/raintomudd/projects/filamentwinder).
- Research, as detailed below

# Resources

- [http://www.8020.net/Design-Tools-31.asp](http://www.8020.net/Design-Tools-31.asp)
- [http://www.cstcomposites.com/about-us/technology/processes/filament-winding-technology/](http://www.cstcomposites.com/about-us/technology/processes/filament-winding-technology/)
- [Composite Filament Winding Machine](https://doc-00-7g-docsviewer.googleusercontent.com/viewer/securedownload/qq8svv1b4ua87k7hhkn8c7o3mntcjmlc/sthcsh3tp4m58p5vnirgs4l4r6t1378r/1376776800000/Z21haWw=/AGZ5hq-UZpm_wNPHSzykgiqan27o/MTQwN2E0NTZhMDU5OTFhZHwwLjQ=?docid=b178c103c4a07976d25fb84bea8b158a%7C72ece9d64d37885d9449209e7a311aa7&chan=EgAAAMrueXuJvkS7FJ6d1r10yC/1PY8JwAXq0A8b0G3RowRp&dom=g.hmc.edu&sec=AHSqidZCGbj67z6ZkAgjQmePEf9T94aVV44k92lLPIqC_N_C0ZMXM7omp-zUA6JIX-Zu4yJ1zl2aJ1Hdx5sd2lIqpYmk1V1MmvxlyhKucNV2EDUGA9CcohNgcn4IFB9_ahP67VN2l2ahnbYDb5h5wvsDP2eUgp177Axx-lbCQzrQCB8QFaNT3V-sYB3ao0K4UDuDDQQWvjZ8JDR7JbAZ9seuBYmPCdzi4La-x3yOMGSW9iW_IE400mEjmxb6fAXg7TyAnx-3FJ2PVdlNbP2qJ-bdf42g4G98Ka8iRXXtSrnJYjQMFl8deYUEUJf9k2D0wco9Co3npfsuPjjNFcZUfYyQGe8zLI19A6e8JWAmiO4FTJ6uQTsGiFU4toZewiyBg6xGUWSV3uYHeFKVzrDcpsQMt1XIrJRgxMlv4vWkyOjGVOIqablFjyirDzBEY72QjQvoBcYEAurrbf15jbxQjgjg5xO2TXx8ENx91rozEBQdPeEX8trpsqFYcPF_1qF_iOGhaigQSptSsro0XS4cpETO5qcVsSm2Og&a=gp&filename=P09226+Conference+Paper.doc&nonce=7a4lfor881kpa&user=AGZ5hq-UZpm_wNPHSzykgiqan27o&hash=kicope4l8v0nol7a4j3dr6ar9ughqfhm)
- [White Paper--Simulating Composite Structures](http://www.ansys.com//staticassets/ANSYS/staticassets/resourcelibrary/whitepaper/wp-simulating-composite-structures.pdf)
- [filamentwinding.pdf](https://drive.google.com/file/d/0B0Jfms0twG8EUU44ZmZsOGhIclE/view?usp=sharing)
- [filamentwinding.pptx](https://drive.google.com/file/d/0B0Jfms0twG8EVnFxQmJqRDdWYzg/view?usp=sharing)
- [filamentwindingtension.pdf](https://drive.google.com/file/d/0B0Jfms0twG8EaHgwaFF6OWdwZ2M/view?usp=sharing)
- [Integration Tools for Design and Process Control of Filament Winding](https://drive.google.com/file/d/0B0Jfms0twG8EM3g1ZUZtRW1vYkk/view?usp=sharing)
- [Model for Wet Filament Winding of Composite Cylinders with Arbitrary Thickness](https://drive.google.com/file/d/0B0Jfms0twG8EOGZwbTJBYVozaUE/view?usp=sharing)

# User Interface

For this system, Sean and I could see one of two paradigms working: you could
either develop a program on the machine itself, or on a computer and then
export a set of commands to the device. Note that reprogramming the
microcontroller every time a new layup schedule is desired is highly
undesirable and as such, not being considered.

Of these two options, using a computer seems much more practical. Not only will
it allow the user to develop the program wherever they want, but it will allow
us much greater programming flexibility. We would have much more computational
power available to us, could choose which language to use, and would then be
able to incorporate a lot more into the end product (i.e. we could run
calculations on the part and estimate its strength). A GUI on the computer
would also be much more user friendly than a bunch of DIP switches or a small
LED display. In addition, the less we do on the PIC, the easier life will be
for us and the more portable (meaning microcontroller-independent) and
extensible the system will be.

However, using this method does add the intermediate steps of exporting,
importing, and interpreting files. While the export and interpretation steps
should be very easy (save to a flash drive and parse a text file respectively),
we do not have any experience reading data off of a flash drive using a PIC
microcontroller.

If USB drive interfacing is easy with the PIC, then we think the GUI would be
the way to go. Otherwise, we will reconsider our other options.

From what we've read, USB interfacing could be "simple." Microchip has a
[write-up](http://ww1.microchip.com/downloads/en/AppNotes/01145b.pdf) on how to
do it, and [additional
hardware](http://electronicdesign.com/dsps/interfacing-usb-flash-drive-pic-microcontroller)
exists to handle it that we could interface with. However, since we currently
don't have access to the hardware to run tests on, we can't be sure.

Once we're back at Mudd (we're currently on winter break), we'll test out USB
interfacing and move forward with the project.
