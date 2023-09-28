---
layout: default
title: Windows
parent: Installing git
grand_parent: Setting up your environment
nav_order: 2
---
# Install Git on Windows

Git for Windows provides a BASH emulation used to run Git from the command line. It also includes graphical interfaces Git GUI and Gitk to manage Git repositories.

Download the latest Git for Windows installer [here](https://gitforwindows.org/).

When you've successfully started the installer, you should see the Git Setup wizard screen. Follow the Next and Finish prompts to complete the installation. The default options are pretty sensible for most users.

Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).

Confirm that you've installed Git correctly by entering the following command in your command line interface:

```bash
git --version
```

You should see the version of the installed Git.

## using Git Bash

![git-bash](../img/git_bash.jpg)

All of the tutorials surrounding `git` will use the bash terminal, it is installed as part of the `gitforwindows` installation and you should be able to find an executable to with a similar logo to the image above.