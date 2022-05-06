---
aliases:
tags: study
---
[[LaTeX]]
# LaTeX Mathematics
*On how to display mathematical equations and formulas in a LaTeX document*

## math mode
In math mode, spaces are ignored and the correct spacing between character is applied.

The two forms of math mode are **inline** and **display**.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
A sentence with inline mathematics: $y = mx + c$
A second sentence with inline mathematics: $5^{2}=3^{2}+4^{2}$

A second paragraph containing display math.
\[
	y = mx + c
\]
\end{document}
```

It's possible to see LaTeX-like mathematical input in other places. MathJax is a system for placing equations in web pages. These systems accept slight variations on LaTeX syntax because they don't actually use a TeX engine.

## inline math mode and mathematical notation
Inline math is marked using a pair of dollar signs. It also accepts `\(...\)`. Simple expressions are entered without any special markup.

Inline math mode restricts vertical size of the expression so that the formula doesn't disturb the line spacing of the paragraph.

*All math* should be marked up as math, even if it's a single character use. For example, `$2$` is math, `2` is not.

### superscripts and subscripts
We can add superscripts and subscripts. They're marked with `^` and `_`.

```latex
Superscripts $a^{b}$ and subscripts $a_{b}$.
```

>[!NOTE]
>You may see examples where simple super- and subscripts are entered without braces, but it's not the official syntax and can go wrong. It's recommended to always use braces.

There's are a lot of specialist math mode commands, like `\sin` and `\log` for sine and logarithm or `\theta` for the Greek letter.

```latex
Some mathematics: $y = 2 \sin \theta^{2}$
```

## display mathematics
The same commands work in display mode. Display mode is centered by default and is meant for larger equations that are 'part of the paragraph'. Display math environments do not allow a paragraph to end withing the mathematics.

The paragraphs should always be started before the display so do not leave a blank line before the environment. If you need multiple lines of math, do not use consecutive display environments, as it produces inconsistent spacing. Instead use a multi-line display environment such as `align` from the `amsmath` package.

```latex
A paragraph about a larger equation:
\[
\int_{-\infty}^{+\infty} e^{+x^2} \, dx
\]
```

Here the sub-/superscript notation is used to set the limits of the integration.

`\,` add some manual spacing between `dx` and the rest of the expression.

Oftentimes you want a numbered equation, which is created using the `equation` environment.

```latex
\begin{equation}
\int_{-\infty}^{+\infty} e^{-x^2} \, dx
\end{equation}
```

The equation number is automatically incremented and may be a simple number as in this example or may be prefixed by section number.

## the `amsmath` package
Mathematical notation is very rich, and the built-in tools that the LaTeX kernel offers sometimes aren't enough. The `amsmath` package extends the core support to cover more.

```latex
Solve the following recurrence for $n,k\geq 0 $
\begin{align*}
	Q_{n,0} &= 1 \quad Q_{0,k} = [k=0]; \\
	Q_{n,k} &= Q_{n-1,k}+Q_{n-1,k-1}+\binom{n}{k} \quad\text{for $n$, $k>0$.}
\end{align*}
```

The `align*` environment makes the equations line up on the `&` like a table. 
We used `\quad` to insert some space and `\text` to insert some normal text inside math mode. We also used `\binom` for a binomial.

`\begin{matrix}` to insert a matrix in the document. Works like a table.

## fonts in math mode
In math mode, font changes convey very specific meaning.
They are written explicitly.