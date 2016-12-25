---
layout: default
title: Backup Scheme
---

I've used several different backup schemes in the past. Currently, I have things set up as follows: 

- **Personal Data:** Any file I've created personally goes into a Google Drive folder which is then synced to the cloud automatically. I also image my data partition every three months onto an external hard drive. 
- **System Data:**  Each partition with an OS on it is imaged every three months (including immediately after the OS is fully configured). The initial image and two most recent images are stored on an external hard drive; the most recent image of my primary drive is also stored on Google Drive. Note that I currently use the free version of [Macrium Reflect](http://www.macrium.com/reflectfree.aspx) for all of my imaging needs. 
- **Versioning:** Google Drive provides versions from the last 30 days. Any file that needs more than that is tracked with Git (and put on GitHub if appropriate). 

With this setup, all of my data is in at least two places: on the appropriate computer (or multiple computers), on an external hard drive (updated quarterly), and possibly in the cloud in Google Drive. Using Google Drive means that I can pull up my personal data on whatever computer I happen to be at; Macrium Reflect makes it very easy to poke around in old images and restore them if need be. And the best part is that I only have to pay for Google Drive (with its very reasonable rates). 
