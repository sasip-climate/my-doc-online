# Formatting tips

## rst format 
You can  write your documentation pages in rst format (close to markdown). See here for some references on the rst syntax: [https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html)


## markdown format
You can also use markdown format if you have switched on the `myst-parser` option in the `conf.py` file. To do so,  add those lines:
  
```
extensions = [
    'myst_parser'
]

source_suffix = {
    '.rst': 'restructuredtext',
    '.txt': 'markdown',
    '.md': 'markdown',
}

myst_enable_extensions = ["dollarmath", "amsmath"]
```

And see [https://myst-parser.readthedocs.io/en/latest/syntax/optional.html](https://myst-parser.readthedocs.io/en/latest/syntax/optional.html) for more info about syntax possibilities


## latex integration

Note that you can already write some nice latex:

$$
   \begin{eqnarray}
      y    & = & ax^2 + bx + c \\
      f(x) & = & x^2 + 2xy + y^2
   \end{eqnarray}
$$

## References
How to do in markdown? Each section/subsection/subsubsection auto-generate achors that you can refer to elsewhere in the text with  `[text of the link](#name-of-your-subsection)`. 

Here is an example of markdown file:

```
* Here i call a famous paper [[1]](#References) in the list of References.
* Here is want to refer to the above [section about latex integration](#latex-integration).
* Here i make reference to another [doc page/section](./build_documentation.md#Set-up-your-documentation).

```

How it renders in html:

* Here i call a famous paper [[1]](#Bibliography) in the list of References.
* Here is want to refer to the above [section about latex integration](#latex-integration).
* Here i make reference to another [doc page/section](./build_documentation.md#Set-up-your-documentation).
* Another way: {doc}`Custom title <build_documentation.md>`

---
## Bibliography

[1] P. Rampal, S. Bouillon, E. Olason, and M. Morlighem. neXtSIM: a new Lagrangian sea ice model.  ́ The Cryosphere, 10:1055–1073, 2016.


