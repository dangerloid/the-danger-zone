---
aliases:
tags: study
---
[[LaTeX]]
# Logical structure
*Going over formatting commands*

LaTeX provides commands to logically structure the document and set the appearance.

## structure and visual presentation
`\emph` gives emphasis to a given part of the text by making it italic (by default).

```latex
Some text with \emph{emphasis and \emph{nested} content}.
Some text with \textit{italic and \textit{nested} content}.
```

`\textit` also makes the text italic, but the difference is that it's *always italic* and doesn't work with nested content.
In some cases, `\emph` doesn't make the text italic, but uses another visual representation for emphasis, like color.

`\textbf` makes the text bold.

## sectioning commands
[[LaTeX vs. Rich Text Formatting]]
Usually, in a word processor, users define sections in a document by taking a string of text and making it larger, or bolder, or of a different color manually. It gets tedious, especially because you have to navigate menus to do that. It slows you down because when you've got to write, *you've got to write*.
LaTeX has handy commands to format sections, and it does it automatically.

>[!NOTE]
>`\section` syntax
>
>```latex
>\section{title}
>lorem ipsum cazzimazzi
>```

```latex
\section{Title of the first section}

Text of material in the first section.

Second paragraph.

\subsection{Subsection of the first section}

Text of material in the subsection.

\section{Second section}

Text of the second section.
```

Using the standard `article` setup, LaTeX numbers the sections and subsections and includes the titles in boldface. It can be changed though.

LaTeX can divide documents in more levels:
- `\chapter`, but it requires `\documentclass{book/report}` for that
- `\section`
- `\subsection`
- `\subsubsection`

Further down is `\paragraph`, which is *not* a way to start new paragraphs, but another section command. It's considered to be "too much" detail.

## lists
To make a list, you start with a `\begin` command and use either `enumerate` or `itemize` to make them ordered and unordered respectively.

>[!EXAMPLE]
>
>```latex
>unordered list
>\begin{itemize}
>	\item item 1
>	\item item 2
>	\item item 3
>\end{itemize}
>
>ordered list
>\begin{enumerate}
>	\item item 1
>	\item item 2
>	\item item 3
>\end{enumerate}
>```

## document titles
There is logical markup for titles, put in the preamble.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
\author{A.~N.~Other \and D.~Nobacon}
\title{Some things I did}
\date{1st April 2020}
\maketitle

Some normal text.
\end{document}
```