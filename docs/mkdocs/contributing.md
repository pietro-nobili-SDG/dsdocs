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

## Project layout

The folder structure is something like this:

```
mkdocs.yml    # The configuration file.
docs/
    index.md  # The documentation homepage.
    ...       # Other markdown pages, images and other files.
```

and it's mostly reflected in the navigation bar on the left,
but it's not required.

To add a new topic, create the folder inside `docs`,
and an `index.md` file for that topic.
For example, to add some info related to Databricks,
which is a general tool,
create

```
docs/tools/databricks/index.md
```

Then add the topic to the navbar:
open `mkdocs.yml`, look for the `nav:` section,
and add the new file

```yaml
nav:
  - Tools: 
    - Databricks: 
      - tools/databricks/index.md
```

As more information is added to the general page for that topic,
at a certain point it makes sense to split it in several pages.
Leave a small introduction on what the tool does in `index.md`
and create more specific files as needed.
Then, add them to the navbar.

```yaml
nav:
  - Tools: 
    - Databricks: 
      - tools/databricks/index.md
      - Scheduling: tools/databricks/scheduling.md
      - Notebook: tools/databricks/notebook.md
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
   