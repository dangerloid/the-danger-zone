---
aliases:
tags: study
---
[[LaTeX]]
# Document classes
*On what document classes are and how they influence the design of the document and the consequent behavior of LaTeX*.

The `\documentclass{...}` command is required in every .tex file and it's always the first command you should have.

## what a document class does
The document class sets up the layout of the final document:

- design: margins, fonts, spacing....
- whether chapters are available
- if the title should be on a separate page

Document classes can also add new commands.
The document class can also set global options for the document, given in square brackets.

## the base classes

LaTeX is supplied with a set od standard classes:

- `article`
	- short document without chapters
- `report`
	- longer document with chapters, single-sided printing
- `book`
	- longer document with chapters, double-sided printing. with front and back matter
- `letter`
	- correspondence with no sections
- `slides`
	- for presentations

The `article`, `report` and `book` classes have similar commands available.

When writing a letter, the commands are a bit different.

`\\` is used to separate the lines of the address and the `letter` class creates a new environment.

`article`, `report` and `book` take the options `10pt`, `11pt` and `12pt` for font size and `twocolumn` for two-column documents.

## function-rich classes
The core classes are very stable, but also conservative in design and range of commands.
The American Mathematical Society provides variants of the standard classed with a more traditional design closer to what's used in mathematics journals.

## presentations
The `slides` class was developed to make physical slides in the mid-1980s.
