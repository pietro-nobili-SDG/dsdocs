---
hide:
  - footer
---
# Unix

## Command Line Interface

You can check out
[a more comprehensive guide](https://tutorial.djangogirls.org/en/intro_to_command_line)
made by the excellent
[Django Girls](https://djangogirls.org/en/)
team.
Skip to the
[summary](https://tutorial.djangogirls.org/en/intro_to_command_line/#summary)
for a quick refresher.
Or literally just
[google it](https://letmegooglethat.com/?q=linux+command+line+tutorial).
There are
[longer tutorials](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview)
and even
[interactive](https://linuxsurvival.com/)
ones.

The Windows tabs refer to PowerShell.

!!! tip

    Press ++tab++ at any point while typing to toggle the autocomplete:
    if there is only one option it will be filled,
    if there is more than one hit ++tab++ again
    to show a list of all the possible options.

### Open the terminal

=== "Linux"

    Press
    ++ctrl+shift+t++
    to open a terminal window.

=== "Windows (PS)"

    Press
    ++windows++,
    type `powershell`
    and open it.

### Learn more about a command

If for some reason Google does not work,
open the manual page for a `command`:

=== "Linux"

    ``` bash
    man [command]
    ```

    Exit the documentation by typing ++q++.

=== "Windows (PS)"

    ``` powershell
    Get-Help [command]
    ```

### Current directory

Print the path to the current directory

=== "Linux"

    ``` bash
    pwd
    ```

=== "Windows (PS)"

    ``` powershell
    pwd
    ```

### List all the files

List all the files and directories.

In the current directory:

=== "Linux"

    ``` bash
    ls
    ```

=== "Windows (PS)"

    ``` powershell
    ls
    ```

In any directory:

=== "Linux"

    ``` bash
    ls path/to/dir
    ```

=== "Windows (PS)"

    ``` powershell
    ls path/to/dir
    ```

!!! note

    The path is relative to the current directory.

    An absolute path is relative to the root of the file system
    (`/` for Linux, `C:` for Windows),
    for example:
    `/home/pmn/repos/dsdocs`.
    So if the current directory is
    `/home/pmn`,
    to list all the files in `dsdocs` run

    ``` bash
    ls repos/dsdocs
    ```

### Change current directory

To change the current directory:

=== "Linux"

    ``` bash
    cd path/to/dir
    ```

=== "Windows (PS)"

    ``` powershell
    cd path/to/dir
    ```

### Create a directory

To create a directory
in the current directory:

=== "Linux"

    ``` bash
    mkdir dir_name
    ```

=== "Windows (PS)"

    ``` powershell
    mkdir dir_name
    ```
