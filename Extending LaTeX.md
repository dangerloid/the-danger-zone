---
aliases:
tags: study
---
[[LaTeX]]
# Extending LaTeX
*On how to use packages to extend LaTeX functionalities*

After having declared a class in the preamble, you can extend LaTeX by adding packages.

## changing how LaTeX works
The LaTeX kernel is limited in user customization, this is when add-on packages extend the functionalities.
The first is to change how LaTeX handles language-specific typesetting through a package called `babel`.

## changing design
It's useful to be able to adjust some aspects of design independent of the document class, like page margins. This can be done through `geometry`.

## defining commands
You can add new commands with `\newcommand`.