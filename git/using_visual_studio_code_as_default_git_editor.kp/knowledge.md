---
title: What is the procedure for setting visual studio code as the default editor for git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: In the command line, run `git config --global core.editor `code --wait``.
---

**Contents**

[TOC]

#Section 1: Installing Visual Studio Code

Visual Studio Code is a popular code editor available for Windows, Mac, and Linux. To install it, simply go to the Visual Studio Code website and download the appropriate version for your operating system.

#Section 2: Setting Visual Studio Code as Default Editor

Once Visual Studio Code is installed, you can set it as the default editor for git by opening a terminal window and typing:

`git config --global core.editor "code --wait"`

#Section 3: Testing the Default Editor Setting

To test that the default editor has been set correctly, type the following command in the terminal window:

`git config --list`

If Visual Studio Code is set as the default editor, you should see a line that says `core.editor=code --wait` 

#Section 4: Using Visual Studio Code with Git

Now that Visual Studio Code is set as the default editor for git, you can use it to edit commit messages and other git related tasks. To do this, simply type the command `git commit` in the terminal window and Visual Studio Code will open with the commit message template.
