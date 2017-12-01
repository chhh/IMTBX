# How to build the website

## MkDocs

### Install dependencies
- Install `Python 2.7`
- the static site generator MkDocs
  - `pip install -U mkdocs`
- fenced code block highlighting
  - `pip install -U pygments`
- Nice markdown extensions for python
  - `pip install -U pymdown-extensions`
- Material design theme for MkDocs
  - System-wide install `pip install -U mkdocs-material`
  - Or just clone the theme repo from GitHub `git clone https://github.com/squidfunk/mkdocs-material.git`. The theme will reside in the folder `mkdocs-material/material`, just copy it and point your `mkdocs.yml` to it like this:
  ```yaml
  theme:
      name: 'material'
      custom_dir: 'themes/material'
      language: 'en'
      palette:
        primary: 'indigo'
        accent: 'indigo'
  ```
  - Also in `mkdocs.yml` you might want to add the following config:
  ```yaml
  docs_dir: 'src'
  site_dir: 'docs'
  ```
  This helps with serving the website using GitHub pages, when it's configured
  to serve contents of `master/docs`

### Create site stub
