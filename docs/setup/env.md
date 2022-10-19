---
hide:
  - footer
---

# Set up the env

## Prerequisites

This guide assumes a minimal level of confidence while using the command line.
If you never did that, read this
[introduction to the command line](../../general/unix).

## Windows Subsystem for Linux

Follow this guide to install the
[Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install)
(WSL).

!!! TODO

    select the latest Ubuntu? or Ubuntu 20.04?

In broad terms, the WSL lets you start a virtual machine with a different operating system running on it, without requiring a dual boot.

## VSCode

Follow this guide to install
[Visual Studio Code](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode)
(VSCode) on Windows.

!!! note

    VSCode is installed on the Windows operating system.
    The
    [Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
    is what lets you access the tools installed on the WSL (e.g. Python, gcc).

!!! TODO

    install a bunch of useful extensions, give a list

## Python

### Managing Python version

On Ubuntu 20.04, the default version of python installed is 3.8.

If you need to install a different version of python,
there are several ways.
Two are reported here.

#### deadsnakes PPA

One of the methods to install a new program on Ubuntu
(and many other Linux distributions)
is with the command `apt install <package_name>`.
There are many programs available in the standard repositories checked by `apt`,
but to install a different version of python you need to add another
[Personal Package Archive](https://help.ubuntu.com/stable/ubuntu-help/addremove-ppa.html.en) (PPA).

The needed one is the
[deadsnakes](https://launchpad.net/~deadsnakes/+archive/ubuntu/ppa)
PPA. Add it with

``` bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
```

Once added, several python-related packages will be available.

``` bash
sudo apt install pythonX.Y       # install pythonX.Y
sudo apt install pythonX.Y-dev   # includes development headers for building C extensions
sudo apt install pythonX.Y-venv  # provides the standard library `venv` module
```

Where `X` and `Y` are the required major and minor version.

#### pyenv

Once set up,
[pyenv](https://github.com/pyenv/pyenv)
lets you install a specific version of python by running

``` bash
pyenv install <version>
```

that you can then use with

``` bash
pyenv shell <version>   # select just for current shell session
pyenv local <version>   # automatically select whenever you are
                        # in the current directory (or its subdirectories)
pyenv global <version>  # select globally for your user account
```

It is very easy to use but the
[installation process](https://github.com/pyenv/pyenv#set-up-your-shell-environment-for-pyenv)
is more involved,
but it is
[clearly explained in this blog post](https://cjolowicz.github.io/posts/hypermodern-python-01-setup/#installing-python-with-pyenv).

### Managing project dependencies

Different projects might require different version of the same python package.
Installing a package system wide is generally a bad idea.

<!-- Virtual environments are Python's solution to this problem.
You can create an environment with different versions of the dependencies
(and even of python)
for each project. -->

#### Venv

The
[venv](https://docs.python.org/3/library/venv.html)
module 
(of the Python standard library)
provides support for creating lightweight “virtual environments” with their own site directories, optionally isolated from system site directories. Each virtual environment has its own Python binary (which matches the version of the binary that was used to create this environment) and can have its own independent set of installed Python packages in its site directories[^1].

You can create a virtual environment with

``` bash
python3 -m venv <venv_name>
```

and use it with

``` bash
source <venv_name>/bin/activate
```

Now, when you run `python` and `pip` commands,
the ones inside the virtual environment will be used.

#### Poetry

<!-- The main drawback of `venv` is that it can only specify -->
Poetry offers more functionalities out of the box compared to venv,
mainly a way to specify dependencies in a looser way,
and some commands to build and publish a package.

## R

You are on your own.

## DBeaver

SQL people suggest using this.
It's useful as it has auto completion of the column names,
and it adds a bunch of useful tools.

Install the
[community edition](https://dbeaver.io/download/)
and set up the
[connection to the database](https://dbeaver.com/2022/03/03/how-to-create-database-connection-in-dbeaver/)
you'll be working on.

## KeePass

It's already installed, use it.

## FZF

Typing ++ctrl+r++
triggers the `reverse-i-search`
in most Linux terminals,
which lets you search through previous commands,
by typing the beginning of the command.

[FZF](https://github.com/junegunn/fzf)
is a general-purpose command-line fuzzy finder,
which lets you filter the history
by typing a non-contiguos substring of the command you are looking for.

For example, if you are looking for the command

```
dbfs cp dbfs:/FileStore/fold/name/results/* local/results/
```

you can type something like `dbcpforeloc`, that is

```
dbfs cp dbfs:/FileStore/fold/name/results/* local/results/
db   cp                 fo        re        loc
```

and probably get the right one.
The list of possible matches is updated after every keystroke,
so just filter them more as needed.

Install it on the WSL with:

``` bash
sudo apt install fzf
```

[^1]: Python docs: [venv module](https://docs.python.org/3/library/venv.html#module-venv)