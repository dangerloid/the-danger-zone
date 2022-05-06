---
aliases:
tags: study
---
[[LaTeX]]
# LaTeX document structure
## writing my first document
This is to see how to use the editor, how the document looks and typeset my source file.
I wrote the example on [LearnLaTeX](https://www.learnlatex.org/):

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.
\end{document}
```

Compiling from the editor doesn't work for some reason and I have to use the CLI for it, but it's not a big deal.
From that I got a simple PDF file that automatically added a page number at the bottom. Handy!

## error handling
Shit happens.
I had trouble with in-editor typesetting but it works now for some reason. I don't want to touch my terminal for this.

## what i've got
The first document shows the basics.
A LaTeX document is made of text and commands. The commands always start with a backslash, with curly braces for arguments and optional ones in square brackets:

>[!EXAMPLE]
>LaTeX command syntax
>```latex
>\command[optional-argument]{argument}
>```

Then you get an output PDF file by telling LaTeX to typeset your plain text.

Every LaTeX document has a `\begin{document}` and an `\end{document}` command. Inside of these commands is the *document body*, or ==content==. In my example code, the body has two paragraphs. You separate paragraphs with one or more blank lines.
Before `\begin{document}` is the *document preamble*, where you put settings and metadata for your file, such as `\documentclass{}` and `\usepackage{}`.

LaTeX has other`\begin{}` and `\end{}` commands; they're called *environments*. They have to match (kind of like [[HTML]] tags).

Comments are made with a `%` sign.

```latex
\documentclass[a4paper, 12pt]{article} % the document class with options
\usepackage[T1]{fontenc}
% comment in preamble
\begin{document}
% comment in document
This is    a simple
document\footnote{with a footnote}.

This is a new paragraph.
\end{document}
```

I added hideous whitespace in one of the paragraphs, but LaTeX still typeset it correctly.

## special characters
Now going over some characters I've already seen:
`\` marks the start of a command;
`{}` mark the mandatory arguments of a command;
`[]` mark the optional arguments of a command.

There are other characters with meaning; `~` marks 'hard' spaces. They don't break over lines and can be useful for cross-referencing.