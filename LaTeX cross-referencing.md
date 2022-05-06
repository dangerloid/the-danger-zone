---
aliases:
tags: study
---
[[LaTeX]]
# LaTeX cross-referencing

When writing a document you may want to refer to numbered items such as figures, tables or equations.

## the `\label` and `\ref` mechanism
LaTeX can remember a spot in the document, but for it to refer to it, you need to label it.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}

\begin{document}
Hey world!

This is a first document.

\section{Title of the first section}

Text of material for the first section.


\subsection{Subsection of the first section}
\label{subsec:labelone}

Text of material for the first subsection.
\begin{equation}
  e^{i\pi}+1 = 0
\label{eq:labeltwo}
\end{equation}

In subsection~\ref{subsec:labelone} is equation~\ref{eq:labeltwo}.
\end{document}
```

>[!WARNING]
>Running pdflatex gives me this error in the CLI
>```bash
>LaTeX Warning: Label(s) may have changed. Rerun to get cross-references right.
>```

In this code block, there are two `\label{}` commands, one after the subsection and one inside the equation environment. They are associated with the last sentence's `\ref` commands. When you run LaTeX, it creates an auxiliary file where information on these labels is stored. When you ask for the reference, LaTeX scrapes it from that file.

The `subsec:` and `eq:` aren't used by LaTeX, it just keeps track of what it has most recently processed. Writing these help remembering the user what that label is for.

If the reference are displayed as `??`, it's because the auxiliary file doesn't get saved on the first run.

The `~` character before the references makes it so that it won't go on a new line when typesetting.

## where to put label
The `\label` command always refers to the previous numbered entity. This means that it should be put after the thing you want to refer to.

## making cross-references into links
You may want hyperlinked cross-references for easier navigation of the document. This can be achieved with the `hyperref` package.