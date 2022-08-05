repository to toy around with ideas to extend and use quarto

## Helpful snippets/links

```
quarto pandoc -f markdown -t json -o ast.json ast.md
```
produces the AST (helpful to see the internal structure before filters are applied)

Open in R with:
```
xfun:::tree(
  jsonlite::fromJSON('ast.json', simplifyVector = FALSE)
)
```
(taken from [here](https://bookdown.org/yihui/rmarkdown-cookbook/lua-filters.html))


## launchbutton

Trying to implement a launch button which allows to run rendered ipynb files to be opened in [google colab](https://colab.research.google.com/?utm_source=scs-index) or other services.

This feature is impemented in [jupyterbooks](https://jupyterbook.org/en/stable/intro.html)

[x] Extend title-block.html and add a yaml variable launch_buttons  
[ ] Via a ipynb-filter

