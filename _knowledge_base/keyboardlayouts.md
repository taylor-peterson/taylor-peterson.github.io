---
title: Keyboard Layouts
---

First off, let me get one thing straight - switching keyboard layouts is not
about speed but comfort/ergonomics. I may eventually exceed my QWERTY speed,
but that's not why I'm looking at changing. I'm looking at changing because I
spend a ton of time on computers and jumping around like crazy on QWERTY is not
the most comfortable thing to do.

While Dvorak and Colemak are excellent alternatives for prose-writing, they do
not make punctuation any more comfortable. Given that much of my work is
punctuation heavy - dev work, scripting, LaTeX - neither will do for me.

As such, I decided to look into custom keyboards. I do not think customizing a
keyboard to be silly. The rationale for this is that in almost every case where
I would be using a keyboard for a reasonable duration, I would have
administrator access and permission from the owner to install my keymap. Plus,
because keystrokes are interpreted locally, this would not affect remote work.

Unfortunately, none of the keyboard generators I've looked at (e.g. ([Keyboard
Evolve](http://www.michaelcapewell.com/programming/keyboardevolve.htm),
[Carpalx](http://mkweb.bcgsc.ca/carpalx/), [Keyboard Layout
Project](http://mathematicalmulticore.wordpress.com/the-keyboard-layout-project/),
[Michael Dickens](https://github.com/michaeldickens/Typing)) move the
punctuation around, which I think is key to getting a programming-appropriate
layout. To make things worse, none of the analyzers I've seen (e.g.
[patorjk](http://patorjk.com/keyboard-layout-analyzer/#/main)) have great
metrics. As such, I'll be looking at making my own layout based on frequencies
found [here](http://xahlee.info/comp/computer_language_char_distribution.html),
[here](http://www.mahdiyusuf.com/post/9947002105/most-pressed-keys-and-programming-syntaxes-2),
and from inputting LaTeX files
[here](http://www.patrick-wied.at/projects/heatmap-keyboard/), then evaluating
and tweaking my keyboard by hand.

One of the most important parameters considered by keyboard modifiers is
keeping the fingers in approximately the same place. Yet, none of them that I
could find fully utilize the easiest to access keys. By adding another modifier
key, you can may all punctuation to the main three rows and make it drastically
easier to access. Dvorak good because it's far more ergonomic than Qwerty, but
also gives me a good starting place to work from regarding symbols.

I've decided to use a heavily modified Dvorak layout. Specifically, I've
swapped the "i" and the "u", remapped backspace to Caps Lock, and added a third
shift state to get all the punctuation in the main area.

I'll add more info about the below layout when I'm more proficient with it.

[![](https://docs.google.com/uc?id=0B0Jfms0twG8EWnAzUGhldFdqMXc&export=download)](https://docs.google.com/file/d/0B0Jfms0twG8EWnAzUGhldFdqMXc/edit?usp=drive_web)

People to send finalized layout to:

- Chris Brown

Layout:

http://www.keyboard-layout-editor.com/#/layouts/355e26b857922ccb878bb1495bad37d1

Keyboard Effort:
http://www.workmanlayout.com/blog/wp-content/uploads/2010/10/keyboard\_graded1.png

Grid Effort: http://www.shenafu.com/code/keyboard/keyboard\_effort\_grid.png

Letter frequency: http://mdickens.me/typing/letter\_frequency.html

More detail: http://mdickens.me/typing/theory-of-letter-frequency.html

Dvorak/Qwerty/Colemak Heatmaps:
https://farm8.staticflickr.com/7003/6554340969\_bb2d63372d\_z.jpg

[![](https://docs.google.com/uc?id=0B0Jfms0twG8ESlJXeUZCLVZXZ00&export=download)](https://docs.google.com/file/d/0B0Jfms0twG8ESlJXeUZCLVZXZ00/edit?usp=drive_web)
