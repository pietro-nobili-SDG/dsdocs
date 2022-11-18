# Improve this guide!

Send help pls.

## Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

For just a couple of useful example visit the
[MkDocs](../guide/)
page in this guide.

## Local development

Install
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/),
clone the repo
and serve the site locally:

```
pip install mkdocs-material
git clone https://github.com/pietro-nobili-SDG/dsdocs.git
cd dsdocs
mkdocs serve
```

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy --force` - [Publish](https://squidfunk.github.io/mkdocs-material/publishing-your-site/#with-mkdocs) the documentation to GitHub pages.
  Or use [GitHub actions](https://squidfunk.github.io/mkdocs-material/publishing-your-site/#with-github-actions).

## Project layout

```
mkdocs.yml    # The configuration file.
docs/
    index.md  # The documentation homepage.
    ...       # Other markdown pages, images and other files.
```

## TODO

1. Header with SDG logo
   (override [partial](https://github.com/squidfunk/mkdocs-material/blob/master/src/partials/logo.html))
1. Footer with link to contributing page
1. Content!
1. `features: - navigation.tabs` is pretty neat,
   if you have a lot of nested level in the navigation sidebar.
   [Docs](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/?h=navigation#navigation-tabs).
   Navigation in general has a lot of useful things.
1. The automatic navigation sidebar is very nice, but it does a lexicographic sort.
   