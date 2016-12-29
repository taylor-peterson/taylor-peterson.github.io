---
title: Jekyll
---

# GitHub Pages Limitations
* Global permalink configuration doesn't work locally (i.e. urls will have
  ".html" appended to them.
* GitHub pages (reasonably) uses the "--safe" option to disable custom plugins
  so they're not executing arbitrary ruby code on their servers. Moreover, the
  set of supported plugins is rather sparse and the alternative of generating
  the site locally and pushing the output instead of the source is distasteful.
* GitHub pages also disallows editing some other settings:
  https://help.github.com/articles/configuring-jekyll/#configuration-settings-you-cannot-change
* You can't have an index page inside a collection - it needs to be a separate page outside.

# Useful Tutorials
* Scrollspy: http://www.codingeverything.com/2014/02/BootstrapDocsSideBar.html
* https://thinkshout.com/blog/2014/12/creating-dynamic-menus-in-jekyll/
* https://www.sylvaindurand.org/compressing-liquid-generated-html/
