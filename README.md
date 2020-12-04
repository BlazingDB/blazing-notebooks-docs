# blazing-notebooks-docs
Repository for documentation about Blazing Notebooks

## Development

I am trying to first build the whole pandas docs before moving to adapting this code to Blazing SQL docs.

```
pip install pydata-sphinx-theme
pip install nbsphinx
pip install gitpython
pip install gitdb
```

To build the docs

```
cd docs && make html
```

The docs will be in the `docs\build\html` folder: open `index.html`.