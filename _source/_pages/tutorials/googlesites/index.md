---
layout: default
title: Google Sites
---

This page will contain the tips and tricks I am picking up in building this
site. See below for miscellany; see the left bar for more involved write-ups.

- As of when I created this site, Google Sites did not support LaTeX, nor did
it have any plans to do so.
[Workaround](http://www.codecogs.com/latex/eqneditor.php)!
- The slideshow on my home page was based on [this
tutorial](http://www.steegle.com/websites/google-sites-howtos/docs-presentation-slider-gadget).

I have since converted my google site to Jekyll using the instructions from
- http://candland.net/2016/02/16/migrate-google-sites-to-jekyll.html

Note that I:
- Leveraged https://github.com/olbat/docker-debian-ruby-nokogiri and replaced
  reverse_markdown with docker run -i <image tag> reverse_markdown
- Had to install ack (http://beyondgrep.com/install/) and tidy (via apt)
- Was still left with a decent amount of cleanup to do
