# Command-Line Interface

A command-line interface (CLI) is a text-based user interface (UI)
used to run programs, manage computer files and interact with the computer[^1].


You can check out
[a more comprehensive guide](https://tutorial.djangogirls.org/en/intro_to_command_line)
made by the excellent
[Django Girls](https://djangogirls.org/en/)
team.
Skip to the
[summary](https://tutorial.djangogirls.org/en/intro_to_command_line/#summary)
for a quick refresher.
[Longer tutorials](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview)
and even
[interactive ones](https://linuxsurvival.com/)
are available.

The Windows tabs refer to PowerShell.

!!! tip

    Press ++tab++ at any point while typing to toggle the autocomplete:
    if there is only one option it will be filled,
    if there is more than one hit ++tab++ again
    to show a list of all the possible options.

<!-- ## Open the terminal

=== "Linux"

    Press
    ++ctrl+shift+t++
    to open a terminal window.

=== "Windows (PS)"

    Press
    ++windows++,
    type `powershell`
    and open it. -->

## Learn more about a command

If for some reason Google does not work,
open the local manual page for a `command`:

=== "Linux"

    ``` bash
    man [command]
    ```

    Scroll down linewise by typing ++j++ or ++arrow-down++
    up with ++k++ or ++arrow-up++,
    and go to the next page with ++space++ or ++page-down++.
    Quit the documentation by typing ++q++.

    Remember, `man` like manual.

=== "Windows (PS)"

    ``` powershell
    Get-Help [command]
    ```

## Current directory

Print the path to the current directory

=== "Linux"

    ``` bash
    pwd
    ```

=== "Windows (PS)"

    ``` powershell
    pwd
    ```

## List all the files

List all the files and directories.

### In the current directory:

=== "Linux"

    ``` bash
    ls
    ```

    Remember, `ls` like list.

=== "Windows (PS)"

    ``` powershell
    ls
    ```

    Remember, `ls` like list.

### In any directory:

=== "Linux"

    ``` bash
    ls path/to/dir
    ```

=== "Windows (PS)"

    ``` powershell
    ls path/to/dir
    ```

!!! note "Absolute vs relative paths"

    An absolute path is relative to the root directory of the file system
    (`/` for Linux, `C:\` for Windows)[^2].
    For example:
    `/home/pmn/repos/dsdocs`.

    A relative path starts from some given working directory,
    avoiding the need to provide the full absolute path.

    In our example,
    if the current directory is
    `/home/pmn`,
    to list all the files in `dsdocs` run

    ``` bash
    ls repos/dsdocs
    ```

## Change current directory

To change the current directory:

=== "Linux"

    ``` bash
    cd path/to/dir
    ```

    Remember, `cd` like change directory.

=== "Windows (PS)"

    ``` powershell
    cd path/to/dir
    ```

    Remember, `cd` like change directory.

## Create a directory

To create a directory
in the current directory:

=== "Linux"

    ``` bash
    mkdir dir_name
    ```

    Remember, `mkdir` like make directory.

=== "Windows (PS)"

    ``` powershell
    mkdir dir_name
    ```

    Remember, `mkdir` like make directory.

## Move a file

Rename or move a file

=== "Linux"

    ``` bash
    mv old_file_name new_file_name
    mv old/file/path new/file/path
    ```

    Remember, `mv` like move.

=== "Windows (PS)"

    ``` powershell
    Move-Item –Path c:\old_path -Destination c:\new_path
    ```

[^1]: TechTarget: [CLI](https://www.techtarget.com/searchwindowsserver/definition/command-line-interface-CLI).
[^2]: Wikipedia: [Absolute and relative paths](https://en.wikipedia.org/wiki/Path_(computing)#Absolute_and_relative_paths).