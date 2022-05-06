---
aliases:
tags: study
---
[[LaTeX]]
# LaTeX formatting
## paragraph spacing
A common style for paragraphs is to not indent them, but instead have a blank line between them. We can achieve that with the `parskip` package.

## forcing a new line
You should not force a new line. You may want a new paragraph on to use `parskip` to put a blank line between paragraphs.

There are a few places to use `\\` to start a new line:
- at the end of table rows
- inside the `center` environment
- in poetry, with the `verse` environment

These are exceptions. You should *not* use `\\` to go to a new line.

## adding explicit space
We can insert a thin space using `\,.`. In math mode there are other commands (`\.,`, `\:` and `\;`) and one for a negative space (`\!`).

Very rarely, like when creating a title page, you may need to add explicit horizontal or vertical space (`\hspace`, `\vspace` they take arguments).

## explicit text formatting
[[LaTeX Logical structure|Logical structure is preferable]], but sometimes you may want to format the text. There are two types of commands to do that, one for short pieces of text and one for 'running' material.

For short text we have:

- `\textbf` for **bold**
- `\textit` for *italic*
- `\textrm` for roman (serif it seems?)
- `\textsf` for sans serif
- `\texttt` for `monospace`
- and `\textsc` for small caps

For running text, we use commands that alter the font setup. They keep running on the whole document, so they must be grouped. The explicit group for this is `{...}`.

You can also set font size like this.