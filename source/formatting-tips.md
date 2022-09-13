# Formatting tips

* **.rst:** You can  write your documentation pages in rst format (close to markdown). See here for some references on the rst syntax: [https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html)


* **.md:** You can also use markdown format if you have switched on the `myst-parser` option in the `conf.py` file. To do so,  add those lines:
  
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


* **latex integration:**

Note that you can already write some nice latex:

$$
   \begin{eqnarray}
      y    & = & ax^2 + bx + c \\
      f(x) & = & x^2 + 2xy + y^2
   \end{eqnarray}
$$
