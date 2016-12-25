<head>
<meta name="generator" content="HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
  <meta http-equiv="Content-Type" content="text/html; charset=us-ascii">

  <title>LaTeX</title>
  <style type="text/css">
ul.c3 {font-family:Tahoma;text-align:-webkit-auto;font-size:medium}
  span.c2 {text-align:-webkit-auto;background-color:transparent}
  span.c1 {font-family:Tahoma;font-size:medium;background-color:transparent}
  </style>

</head>

# LaTeX

  

| 
  

 | 

Misc. LaTeX Wisdom

- Don't use $$...$$ - it is a Plain TeX command. It will modify vertical spacing within formulas, rendering them inconsistent. Instead, use \[...\] or \begin{equation\*}...\end{equation\*} (Source:Â [obsolete commands and packages](http://mirror.utexas.edu/ctan/info/l2tabu/english/l2tabuen.pdf)) 
- For one-liners, use equation over align because equation will add less vertical space ([Source](http://tex.stackexchange.com/questions/321/align-vs-equation)) 
- Align is preferred for multi-line equations.
- Use hyperref's \autoref{..} to avoid typing Section \ref{...} as it will automatically add in the correct preceding word.Â 
- Put each sentence on a new line. This makes finding errors much easier.Â 

 | 
  

 |

  

