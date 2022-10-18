---
hide:
  - footer
---

# Set up the env

## Prerequisites

This guide assumes a minimal level of confidence while using the command line.
If you never did that, read
[this guide](../../general/unix).

## Windows Subsystem for Linux

Install the Windows Subsystem for Linux (WSL),
following
[this guide](https://learn.microsoft.com/en-us/windows/wsl/install).

In broad terms, the WSL lets you start a virtual machine with a different operating system running on it, without requiring a dual boot.

## VSCode

Install Visual Studio Code (VSCode),
following
[this guide](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode).

Please note that VSCode is installed on the Windows operating system.
The
[Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
is what lets you access the tools installed on the WSL (e.g. Python, gcc).

TODO install a bunch of useful extensions

## Python

### Poetry

venv?

## DBeaver

SQL people suggest using this.
It's useful to have auto complete of the column names,
and adds a bunch of useful tools.

Install the
[community edition](https://dbeaver.io/download/)
and
[set up](https://dbeaver.com/2022/03/03/how-to-create-database-connection-in-dbeaver/)
the connection to the database you'll be working on.

## KeePass

It's already installed, use it.
