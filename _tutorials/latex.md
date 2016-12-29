---
layout: default
title: LaTeX
---

Misc. LaTeX Wisdom

- Don't use $$...$$ - it is a Plain TeX command. It will modify vertical spacing within formulas, rendering them inconsistent. Instead, use \[...\] or \begin{equation\*}...\end{equation\*} (Source: [obsolete commands and packages](http://mirror.utexas.edu/ctan/info/l2tabu/english/l2tabuen.pdf))
- For one-liners, use equation over align because equation will add less vertical space ([Source](http://tex.stackexchange.com/questions/321/align-vs-equation))
- Align is preferred for multi-line equations.
- Use hyperref's \autoref{..} to avoid typing Section \ref{...} as it will automatically add in the correct preceding word.
- Put each sentence on a new line. This makes finding errors much easier.
