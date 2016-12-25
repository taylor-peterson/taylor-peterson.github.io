<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>Programming Principles</title>
  <style type="text/css">
span.c1 {background-color:transparent}
  </style>

</head>

# Programming Principles

  

| 
  

 | 

- Blocks inside conditionals and loops should preferably be one line long and have descriptive names to improve readability and self-documentation 
- Limit the number of arguments to functions (0 is best; flags are terrible) 
- Comments are crutches for unclear code 
- Only the code is guaranteed to be true - code should be its own documentation
- Replace comments with a function name that says the same thing
- No need for comments in non-public methods/classes - you can just look at the code itself
- That said, comments can be useful for informative explanation of intent, amplification of important, API documentation, etc.Â 
- Write tests to learn API's (bonus: documentation & feature checking)

 | 
  

 |

  

