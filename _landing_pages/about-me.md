---
title: About Me
---

[LinkedIn](http://www.linkedin.com/pub/taylor-peterson/80/b19/aa8/)

Email:

tayloredwardpeterson [at] gmail [dot] com

Hello. My name is Inigo Montoya. You killed my father. Prepare to die.

Wait... that's not right. My name's actually Taylor Peterson. My father is
doing quite well. And the only thing you have to prepare yourself for is
_science and awesomeness_. Because that's pretty much all you're going to find
on this website.

So about me. I'm a robotics aficionado with a lifelong love of learning. I
graduated with a double major in Engineering and Computer Science from Harvey
Mudd College and am off to work with Amazon Prime Air.

When I'm not at work, you can usually find me working on one of my many
projects. Sometimes that means I'm coding up or testing an algorithm on a
robot. Other times, you can find me designing and fabricating parts. I do a bit
of everything.

In the precious little time left over after school work and projects, I'll be
out swimming, cycling, or running. Well, that or asleep.

Enough about me, check out the rest of the site to see what I've been up to
lately.

![https://docs.google.com/file/d/0B0Jfms0twG8EVG5GQ1BDbV93Rmc/edit?usp=drive_web](https://drive.google.com/uc?id=0B0Jfms0twG8EVG5GQ1BDbV93Rmc){:width="100%"}

That's me wondering why you're still on this page and not looking at the rest
of the site.


{% for page in site.about_me %}
    {% assign page_url_parts = page.url | split: '/' %}
    {% assign page_url_parts_size = page_url_parts | size %}
    {% if page_url_parts_size == 3 or page.path contains 'index' %}
# [{{ page.title }}]({{ page.url }})
[![{{ page.title }}]({{ page.image_path }}){:height="200px"}]({{ page.url }})
    {% endif %}
{% endfor %}
