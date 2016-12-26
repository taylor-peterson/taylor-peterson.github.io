---
layout: default
title: Naming/Versioning
---

When it comes to naming and version control for SolidWorks files, I generally agree with [Sean's recommendations](https://sites.google.com/site/raintomudd/tutorials/solidworks-namingandversions). 

That said, I differ in how I assign version numbers. Instead of starting at 1.0, then increasing by 0.1 until there is a major change or the revision is at x.9, I use a modified set of [Semantic Versioning](http://semver.org/) guidelines: 

- Start at 0.1.0
- Then, given a version number MAJOR.MINOR.PATCH, increment the:

1. MAJOR version when you make backwards-incompatible<sup><span class="c3">[1]</span></sup> changes (or set to 1.0.0 when machining starts)
2. MINOR version when you add backwards-compatible functionality
3. PATCH version when you make backwards-compatible fixes

I find that handling version numbers in this way gives you a better idea of what has changed from revision to revision, whether or not different parts will be compatible, and where things are in production. 

[1] The idea here is that all parts with the same MAJOR version number should work together at all times. 
