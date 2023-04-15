---
title: Configuring and utilizing meld as your git diff and merge tool
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git config --global diff.tool meld` and `git config --global merge.tool meld` to set Meld as your git difftool and mergetool.
---

**Contents**

[TOC]

### Installing Meld

Meld is a graphical diff and merge tool that is available for Linux, macOS, and Windows. To install Meld on Linux, open a terminal window and enter the following command:

`sudo apt-get install meld`

For macOS, you can install Meld using Homebrew:

`brew install meld`

For Windows, you can download the installer from the Meld website.

### Setting up Meld as the Default Diff Tool

To set up Meld as the default diff tool for Git, open a terminal window and enter the following command:

`git config --global diff.tool meld`

This will set Meld as the default diff tool for all of your Git repositories.

### Setting up Meld as the Default Merge Tool

To set up Meld as the default merge tool for Git, open a terminal window and enter the following command:

`git config --global merge.tool meld`

This will set Meld as the default merge tool for all of your Git repositories.

### Using Meld

Once you have installed and configured Meld as the default diff and merge tool for Git, you can use it to compare and merge files. To compare two files, open a terminal window and enter the following command:

`git difftool <file1> <file2>`

To merge two files, open a terminal window and enter the following command:

`git mergetool <file1> <file2>`
