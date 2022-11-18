# MkDocs + material

Basic 
[MkDocs](https://www.mkdocs.org)
and
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
guides.

## Tips

!!! note

    Use a single `# Header` per page, or the Table of Content will disappear.

## Reference

Material for MkDocs has a lot of
[interesting features](https://squidfunk.github.io/mkdocs-material/reference/).
In this page there is an overview of some of them.

The source code to generate this examples is not shown,
either check the
[source code of this page](https://raw.githubusercontent.com/pietro-nobili-SDG/dsdocs/main/docs/mkdocs/guide.md)
or follow the links in the headers to check the official documentation.

### [Admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)

Useful to include side content without significantly interrupting the document flow:

!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

### [Code blocks](https://squidfunk.github.io/mkdocs-material/reference/code-blocks/)

With title, line numbers and highlighted lines.

``` py linenums="1" title="bubble_sort.py" hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

With code annotations (click the fancy `+` sign):

``` yaml
theme:
  features:
    - content.code.annotate # (1)!
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.


### [Math](https://squidfunk.github.io/mkdocs-material/reference/mathjax/)

Easily write equations.

$$
\operatorname{ker} f=\{g\in G:f(g)=e_{H}\}{\mbox{.}}
$$

Or use it inline:
The homomorphism $f$ is injective if and only if its kernel is only the 
singleton set $e_G$, because otherwise $\exists a,b\in G$ with $a\neq b$ such 
that $f(a)=f(b)$.

### [Content tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/)

Group alternative content under different tabs.
Content tabs can be linked so that when clicking on a label all the tabs will switch:

=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

<!-- no idea how to split them properly but this works -->

=== "C"

    ``` c
    // more C code
    ```

=== "C++"

    ``` c++
    // more C++ code
    ```

### [Lists](https://squidfunk.github.io/mkdocs-material/reference/lists/)

On top of the standard ordered and unordered lists,
material offers:

#### [Definition](https://squidfunk.github.io/mkdocs-material/reference/lists/#using-definition-lists) lists:

`key`

: value

`other key`

: other value

#### [Task](https://squidfunk.github.io/mkdocs-material/reference/lists/#using-task-lists) lists:

- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque

### [Abbreviations](https://squidfunk.github.io/mkdocs-material/reference/tooltips/#adding-abbreviations)

Define a glossary (in a single file `includes/abbreviations.md`),
and use it everywhere:
QUTSUC.

### [Keyboard keys](https://squidfunk.github.io/mkdocs-material/reference/formatting/?h=ctrl#adding-keyboard-keys)

Render neatly key combos like
++ctrl+alt+del++
or
++ctrl+shift+t++.
Check out the
[full list](https://facelessuser.github.io/pymdown-extensions/extensions/keys/#extendingmodifying-key-map-index)
of keys available.

### [Footnotes](https://squidfunk.github.io/mkdocs-material/reference/footnotes/)

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.

[^2]:
    [Lorem ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum)
    dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy --force` - [Publish](https://squidfunk.github.io/mkdocs-material/publishing-your-site/#with-mkdocs) the documentation to GitHub pages.
  Or use [GitHub actions](https://squidfunk.github.io/mkdocs-material/publishing-your-site/#with-github-actions).
