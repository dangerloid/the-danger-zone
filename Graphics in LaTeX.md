---
aliases:
tags: study
---
[[LaTeX]]
# Graphics in LaTeX
*How to include external graphic files and position them*

To include graphics from outside LaTeX, I need the `graphicx` package, which adds the command `\includegraphics` to LaTeX.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}

\begin{document}
This picture
\begin{center}
	\includegraphics[height=2cm]{example-image}
\end{center}
is an imported PDF.
\end{document}
```

>[!NOTE]
>Supported formats:
>EPS, PNG, JPG, PDF
>If you have more than one version of the graphic, specify the extension, otherwise the engine will guess the file.

## altering graphic appearance
The `\includegraphics` command has many options to control the size and shape of the image.

The most obvious thing to set is the `height` or the `weight` of an image, which are often relative to the `\textwidth` or `\linewidth`.
You can also `scale` images or rotate them by an `angle`.

## making images float
In typesetting, especially with technical documents, graphics may move to another spot in the document. This is a *float*, concept that exists in [[CSS]] as well. Images are included as floats so that they don't leave big empty gaps in the page.

Floats are included in square brackets in the `\begin{figure}` command. The options are:

- h - here
- t - top of the page
- b - bottom of the page
- p - a dedicated page only for floats


## on naming files
The cross-platform nature of LaTeX requires the user to put thought on file naming. The safest way to name files is to make them simple and without spaces.