---
layout: default
title: Solidworks
---

# Overview

More content will be added soon, but for now, here are some quick thoughts:

- Naming should generally not have the version in it. That goes as a property
  field in the file itself.
- Hole wizard takes a bit of getting used to but is helpful
- Mirror whenever possible (and use the related symmetry)
- Stick to ISO standards
- Shortcuts are your friend (M for measure, D for dimension, C for constrain,
  and so on). Saves time.
- Use cosmetic threads over actually threading the part - it will make
  rebuilding and simulation faster
- To make a plane offset from another plane by a set angle, use the define
  geometry feature and select the plane to offset from and the axis of revolution
- When possible, use a revolved boss/base to start off the part
- Define features relative to a set origin. This makes future edits easier and
  is what you will want to show in drawings.

# Naming/Versioning

When it comes to naming and version control for SolidWorks files, I generally
agree with [Sean's
recommendations](https://sites.google.com/site/raintomudd/tutorials/solidworks-namingandversions).

That said, I differ in how I assign version numbers. Instead of starting at
1.0, then increasing by 0.1 until there is a major change or the revision is at
x.9, I use [Semantic Versioning](http://semver.org/) guidelines. Note that if a
part has already been machined, it should probably already be at 1.0.0+.

I find that handling version numbers in this way gives you a better idea of
what has changed from revision to revision, whether or not different parts will
be compatible, and where things are in production.
