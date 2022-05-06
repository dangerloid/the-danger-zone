---
aliases:
tags: study
---
[[LaTeX]]
# LaTeX Tables
Tables are set using the `tabular` environment.

To typeset a `tabular` we need to tell LaTeX how many columns will be needed and how they should be aligned.

```latex
  Animal & Food  & Size   \\
  dog    & meat  & medium \\
  horse  & hay   & large  \\
  frog   & flies & small  \\
```
Aligning `&` and  `\\` isn't necessary but helps with source readability.

If you have a lot of text in a column, it won't go on a new line on its own.
Using a `p` column, will set it as a paragraph and treat it as such.

If your table has many columns, you can shorthand the argument as `*{num}{string}`. Therefore, `*{6}{c}` is the equivalent of `{cccccc}`.

## adding rules (lines)
Lines should be using sparsely in tables. Vertical lines can look unprofessional. For professional tables you shouldn't use any of the standard lines, and it is wise to learn the `booktabs` package.
It adds a four different types of lines:

- `\toprule`
- `\midrule`
- `\cmidrule{num-num}`
- `\bottomrule`

## merging cells
You can merge cells horizontally by using `\multicolumn`.  It has to be used first thing in a cell. It takes three arguments:
- the number of the cells which should be merged
- the alignment of the merged cell
- the contents of the merged cell

Merging vertically doesn't have native support. It suffices to leave empty cells to give the reader the correct meaning of the table.