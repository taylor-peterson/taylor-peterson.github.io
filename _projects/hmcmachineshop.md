---
title: HMC Machine Shop
status: completed
dates: 2012/01-2015/05
image_path: projects/hmcmachineshop/fullShop.jpg
---

# Overview

I started working as a proctor in Harvey Mudd's machine shop the spring of my
sophomore year. In this role, I was responsible for supervising non-proctors
and ensuring safe practices, cleanliness, and proper use of all machines.

{% include image.html
    path="projects/hmcmachineshop/fullShop.jpg"
    caption="Mudd's machine shop - I'm in the apron on the left."
%}

In the summer after my sophomore year, I became an Associate Head Shop Proctor
(i.e. a student assistant manager of the machine shop). In this capacity, I
worked with Sean Messenger (the other AHSP), James Best and Jason Bluhm (Head
Shop Proctors), Paul Stovall (Shop Manager), Prof Gokli (E4 Instructor), and
Prof Spjut (Clinic Director) to organize the staffing and operation of Mudd's
machine shop.

I was promoted to Head Shop Proctor after the end of my junior year and
continued working to improve the shop with Sean Messenger, Paul Stovall, Prof
Gokli, Prof Spjut, and our AHSPs - Richard Piersall and Suzy Kim. One of the
biggest things I focused on was institutionalizing our changes so that the
shop would continue to improve.

Improving the machine shop is an ongoing project that I
was heavily involved in. To see what got the project started, check out [Shop
Reform]({{ page.url}}#shop-reform). For pretty
pictures and an idea of how much has changed once Sean and I got involved, take
a look at [Shop
Organization](https://sites.google.com/site/raintomudd/projects/machineshoporganization).
[Prof Hammer]({{ page.url }}#prof-hammer) is a
fun project Sean and I ran over the summer after our sophomore year to get
professors of all departments in the machine shop.

# Shop Reform

Before I became a shop proctor, I had noticed many issues with the way the shop
was run. For example, every proctor gave different advice, the shop was
extremely disorganized, and it wasn't easy to learn about more advanced
machining processes.

Once I became a shop proctor, I came to realize why this was happening: shop
proctors received virtually no training and no one was taking ownership for
improving the shop. I felt that this needed to change and contacted the current
Head Shop Proctors (student managers of the shop) to try to start making
improvements, but nothing came out of it.

While many other students shared my views on the shop, few were willing to help
out and had the time to do so. However, Sean Messenger was willing to join me
in shaping up the shop. We both thought it was high time someone did something
to change the state of things. So, starting in the summer after our sophomore
year, that's exactly what we started doing.

In the following years, Sean and I actively pushed for shop reform
(e.g. cleanliness, organization, and (most importantly) training for the shop
proctors).

One of our first steps was to improve the training of proctors. To that end, we
[petitioned](https://docs.google.com/file/d/0B-N_AdkrDR3jdUY4Njc0WThwekk/edit?usp=sharing)
the school to pay for professional training of a few of the more experienced
and dedicated shop proctors, intending those individuals to go on and train the
rest of the shop proctors. After considering our proposal, the engineering
department decided to keep things in house and have the school machinist train
us on a weekly basis during the summer.

In response to our requests, Paul developed a curriculum for all proctors and
used us as guinea pigs to test it out. We learned a ton in the process, have
used that knowledge to help others, and worked on improving the training
process.

In addition to proctor training reforms, Sean and I started to tackle shop
organization over the summer. After discussions with the faculty in charge of
the shop, we took responsibility for implementing 5S methodologies in the shop
to improve safety, better organize materials and equipment, and create a better
working environment. For more information on this project and lots of pictures,
check out Sean's write-up
[here](https://sites.google.com/site/raintomudd/projects/machineshoporganization).

One of the big things we learned through the process is that _it is absolutely
essential to include everyone who uses the shop in any significant changes_.
Sean and I had come in with the (in hindsight, somewhat silly) idea that people
would love all of the changes we were making. While that was generally true,
there were a few contentious changes (e.g. removing the large piles of wood
scraps) and several proctors had differing views on what the ideal shop looked
like.

Once we realized we needed to involve others more, Sean and I made extensive
efforts to get feedback on the changes we were making and dynamically altered
what we were doing in response to those suggestions. When the fall semester
started, we gave presentations to the shop proctors about why we thought all
the individual changes were justified and then took (and implemented) even more
suggestions from these discussions.

We also organized a monthly open shop meeting for anyone on campus to voice
concerns or suggestions in person. This meeting was supplemented with an online
form that anyone could use to comment on the changes or the current status of
the shop. We also hosted a monthly proctor meeting. Whether it was us bribing
them with pizza or the proctors just being more involved (more the latter than
the former), we got the most feedback from these sessions.

The shop has stayed much cleaner than it has been in the past, and more and
more students are getting advanced training. All told, it looks like our
changes have taken hold and we have finally started the ball rolling!

# Shop Organization

A big part of our work in the shop has been improving organization. Typically,
this has been done by implementing visual controls. For example, putting tools
on pegboards and tracing their outlines so it's clear what's missing. Another
thing we've done is arrange all work stations such that they now contain all
tools used in common use such that everything is clearly visible and missing
tools stand out. Mill station 2, as shown below is a great example of this.

{% include image.html
    path="projects/hmcmachineshop/studentshop14-54.jpg"
    caption="Mill station 2."
%}

Another major change we made was to add cameras to each shop. After some setup
(including routing a couple hundred feet of ethernet cable through the
ceilings) we had a monitor setup in the main shop which allows proctors to
monitor activity in the other two shops. While this by no means obviated the
need to physically go to the other shops to check on students, it's definitely
better than in the past when proctors had no idea what was going on in the
other shops.

After getting fed up with the old check in system (which consisted of manually
checking if a student was cleared on a spreadsheet hosted on a very, very slow
computer), I took lead creating an automated check-in system (joined by Richard
Piersall and later on Alex Ozdemir). A mostly complete version of the system
may be seen below.

{% include image.html
    path="projects/hmcmachineshop/check_in_front.jpg"
    caption="The front of the check-in board showing several IDs in place."
%}

The system works by taking user input via buttons and a card swipe. This
information is transmitted to a computer running a python script which
communicates with the Google spreadsheet containing the shop user list. The
process of checking in a user is reduced to a few button presses and card
swipes. While there's still a ways to go to smooth out the kinks as of now, the
system has some huge benefits that make it worth all the work (e.g. tracking
shop usage, being able to display machine use live).

Making the board itself was definitely a hassle. As you can see in the image of
the back of the board below, there are a ton of pieces involved. In particular,
getting the plastic panels to sit flat and properly adjusting all of the
microswitches were major pains.

{% include image.html
    path="projects/hmcmachineshop/check_in_back.jpg"
    caption="The back side of the check-in system."
%}

# Prof Hammer

One day, when Sean and I were wandering the halls, we ran into Dean Jacobsen
(Professor of Mathematics and Dean of Students) outside of the machine shop and
Sean asked him if he had ever considered making a hammer (a traditional project
for engineering majors at Mudd). Turns out, he had always wanted to make one,
but never had the opportunity, so Sean and I offered to help him and any other
professors that might be interested.

The idea of teaching the professors and helping them make hammers got Sean and
I excited and we ran around inviting everyone we thought we be interested.
Turns out a lot of professors wanted to make hammers and quite a few shop
proctors were willing to help out! So we went to the engineering department and
pitched the idea. They approved, so off we went.

{% include image.html
    path="projects/hmcmachineshop/Saeta_Hammer_Gif.gif"
    caption="The always amusing Professor Saeta and his completed hammer."
%}

In the end, only a handful of the original group (Profs Gokli, Saeta, and Yong)
finished their hammers, but we hope that more professors will get a chance to
make a hammer in the future.

# CNC Mill Collet Holder

Sean and I done goofed and ordered non-laser-cuttable material for a few shop
projects (we were positive that polycarb was laser-cuttable but apparently it
flames up if you try to cut it... oops). But it was substantially cheaper and
more durable as opposed to the laser-cuttable stock, and shipping was rather
expensive, so we decided to deal with it and machine the parts instead.

See below for an image of one of the sketchy fixturing jobs we had to do
(because we were out of double-sided tape and because I didn't cut the part
oversize (because I didn't realize we were out of that tape... (one more set of
parentheses to bug Sean (and a smilie to make things even better :) )))).

{% include image.html
    path="projects/hmcmachineshop/sketchyFixturing.jpg"
    caption="Sketchy fixturing."
%}

Check out [this
video](https://drive.google.com/file/d/0B0Jfms0twG8ENHVfRnJuUlVON00/view?usp=sharing)
of the machining process. Gotta love the plastic everywhere - looks like it
snowed in the shop.
[This](https://drive.google.com/file/d/0B6O1HmBYn-U8bWhIMlVGRzJ1NVk/edit?usp=sharing) is
a better video of the actual machining. We're running the mill at 5000 RPM
(it's maximum speed) at 20 IPM.

{% include image.html
    path="projects/hmcmachineshop/plasticEverywhere.jpg"
    caption="Plastic everywhere..."
%}

Finally, below is a picture of the collet holder. You can't see it, but we
rastered on labels for each size (rastering is using the laser-cutter to etch
the surface - makes it look like frosted glass). If you ask me, the final
product is way better than the previous system!

{% include image.html
    path="projects/hmcmachineshop/oldVsNew.jpg"
    caption="The old (left) and the new (right). One looks a bit better if you ask me..."
%}

So in the future, we're going to be more careful about what material we order,
and check to see if we have all the tools we need. I don't know if you can see
it, but there are also two lines we accidentally made in the material by not
deburring all of our sacrificial plates. So we gotta do that better too.
Learning things! Yay!
