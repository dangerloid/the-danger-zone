---
aliases:
tags: study
---
[[LaTeX]]
# LaTeX citations and references

You *could* include bibliographic citations directly in the document, but you can retrieve them from an external file. This is a database of references, containing the information in a processing-friendly format.

## reference databases
Also referred as BibTex files, they have a `.bib` extension. They contain one or more entries and a series of fields for each one.

Here's an example:

```latex
@book{Graham1995,
  author    = {Ronald L. Graham and Donald E. Knuth and Oren Patashnik},
  title     = {Concrete Mathematics},
  publisher = {Addison-Wesley},
  year      = {1995},
}
```

