<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>Naming/Versioning</title>
  <style type="text/css">
div.c5 {font-size: 70%; text-align: left}
  div.c4 {margin-left: 2em}
  span.c3 {font-size: 70%}
  span.c2 {background-color:transparent}
  span.c1 {font-size: 80%}
  </style>

</head>

# Naming/Versioning

  

| 
  

[Solidworks Main](https://sites.google.com/site/tayloredwardpeterson/tutorials/solidworks)

  

[Templates/Properties](https://sites.google.com/site/raintomudd/tutorials/solidworks-templatesandproperties)
  

[Naming/Versioning](https://sites.google.com/site/tayloredwardpeterson/tutorials/solidworks/namingversioning)

 | 
 When it comes to naming and version control for SolidWorks files, I generally agree with [Sean's recommendations](https://sites.google.com/site/raintomudd/tutorials/solidworks-namingandversions). 
  

 That said, I differ in how I assign version numbers. Instead of starting at 1.0, then increasing by 0.1 until there is a major change or the revision is at x.9, I use a modified set of [Semantic Versioning](http://semver.org/) guidelines: 

- Start at 0.1.0
- Then, given a version number MAJOR.MINOR.PATCH, increment the:

1. MAJOR version when you make backwards-incompatible<sup><span class="c3">[1]</span></sup>Â changes (or set to 1.0.0 when machining starts)
2. MINOR version when you addÂ backwards-compatibleÂ functionality
3. PATCH version when you make backwards-compatible fixes

 I find that handling version numbers in this way gives you a better idea of what has changed from revision to revision, whether or not different parts will be compatible, and where things are in production. 

  

  

  

  

  

 [1] The idea here is that all parts with the same MAJOR version number should work together at all times.Â 

 | 
  

 |

  

