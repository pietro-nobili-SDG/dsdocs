# Improve this guide!

Send help pls.

## Local development

Install
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/),
clone the repo
and serve the site locally:

```
python3 -m venv venv
source venv/bin/activate
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

### Add a markdown page

To add a new topic, create the folder inside `docs`,
and an `index.md` file for that topic.
For example, to add some info related to Databricks,
which is a general tool,
create the file

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

This will result in a navbar that has togglable a `Databricks` entry:
when clicked, the `databricks/index.md` page will be shown,
and the nested labels will be shown.

### Add a html page

To link an external html page,
add the `.html` file in the same folder where the link will be used

```
docs/tools/databricks/interactive.html
```

and simply refer to it in a markdown file:

```
[link text](./interactive.html)
```

## Material for MkDocs

For the full documentation visit [MkDocs](https://www.mkdocs.org)
and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

For a short gallery of useful mkdocs-material features visit the
[MkDocs + material](../guide/)
page in this guide.

## TODO

1. Header with SDG logo
   (override [partial](https://github.com/squidfunk/mkdocs-material/blob/master/src/partials/logo.html))
1. Footer with link to contributing page
1. Content!
1. `features: - navigation.tabs` is pretty neat,
   if you have a lot of nested level in the navigation sidebar.
   [Docs](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/?h=navigation#navigation-tabs).
   Navigation in general has a lot of useful things.
   