---
layout: page
title: Hardware
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

## In addition to working on software, I design and manufacture new hardware. In particular, I have redesigned the hydrophone mounting hardware and retrofitted the [kort nozzle](http://en.wikipedia.org/wiki/Ducted_propeller) and rudder. 

Note that pictures of the new system will be added around the third week of January when I regain access to the lab. 

### Hydrophone Mounting Hardware

In order to get useful localization data, the hydrophones must be offset from the body of the Iver by approximately 0.4 meters and at a spacing of 2.4 meters. The offset from the body of the Iver is to avoid interference from the propeller and ensure that the sensors remained submerged during surface runs; the spacing is necessary to get adequate angular resolution. 

The old system made use of foam padding and hose clamps to hold a single-piece PVC frame to the Ivers. The hydrophones and their cables were then taped to the frame. 

[![http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/1209est-robot-headon-gwen-goodmanlowe-07.jpg](http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/1209est-robot-headon-gwen-goodmanlowe-07.jpg)](http://cdn.abclocal.go.com/images/kabc/cms_exf_2007/news/local/los_angeles/1209est-robot-headon-gwen-goodmanlowe-07.jpg)

In the past, the hydrophones were attached to the AUV using a lot of tape, foam, strap clamps, and a single-piece PVC frame. 

This system was bulky (both to transport and hydrodynamically), took forever to set up or tear down, and looked terrible. 

I ended up machining mounting brackets to attach the hydrophone frame to the AUVs' racks. I then mocked up a modular frame out of PVC as a prototype. This frame was able to break down into a small bundle that was much easier to transport than the previous frame. To make tape unnecessary, I designed mounting brackets for the hydrophones and clips to attach the cables to the frame. To top it all off, Hannah shortened up the cables. 

[![https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EUVhHemJwVFE1VFU)](https://docs.google.com/file/d/0B0Jfms0twG8EUVhHemJwVFE1VFU/edit?usp=drive_web)

The current system uses a modular PVC frame, 3D printed hydrophone holders, custom-machined mounting hardware, and laser-cut delrin cable holders. 

Previously, assembling the frame took close to 15 minutes of fumbling around and a headache. With the prototype system, it was as simple as threading together a few parts, sliding the hydrophones in place and tightening them down, then snapping the cord into the holders. Not only is it a lot easier and less painful, it's less wasteful too! 

One thing that I forgot to consider was that removing all of the foam previously in the mounting system drastically affected the buoyancy of the Ivers. The first time we tested out the new mounting system, the Iver sunk! Fortunately, it was only in a few feet of water, so we didn't lose it. But it was in Phake Lake in the Bernard Field Station and that water is gross, so I wasn't too happy about having to dive in after it. Afterwards, we were able to take out some of the ballast and the Ivers achieved neutral buoyancy once again. 

Unfortunately, the current prototype system is not sufficient for extended use - while the cord holders are durable enough for continued use, the 3D printed hydrophone holders and PVC frame have not held up well. Repeatedly tightening and loosing the screws in the holders eventually causes them to fall apart; the joints on the PVC frames are not flush, making them a major stress riser that will fail if the Ivers are transported with the frames attached (the bouncing motion is too much for the PVC to withstand). 

That said, work is in progress to replace the 3D printed parts with machined ones and the PVC frame with a carbon fiber one. 

### Kort Nozzle and Rudder

I also modified the existing rudders in order to be able to attach the long absent kort nozzles and thereby improve the speed and efficiency of the Ivers. In order to attach them, I also had to manufacture new support struts for the nozzles - the old ones were bent out of shape during transport on an earlier mission. 
