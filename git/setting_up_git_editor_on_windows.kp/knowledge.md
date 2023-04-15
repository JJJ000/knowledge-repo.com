---
title: What steps do I need to take to configure an editor to use with git on a windows system?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Download and install a Git-compatible text editor, such as Visual Studio Code, Atom, or Sublime Text.
---

**Contents**

[TOC]

1. **Install Git**

Before you can use Git, you must install it on your Windows machine. You can download the latest version of Git from the [Git website](https://git-scm.com/downloads). Follow the instructions to install Git on your machine.

2. **Choose an Editor**

Once Git is installed, you need to choose an editor to work with it. Popular editors for Windows include [Atom](https://atom.io/), [Sublime Text](https://www.sublimetext.com/), and [VSCode](https://code.visualstudio.com/). Download and install the editor of your choice.

3. **Configure Git with Editor**

Once the editor is installed, you need to configure Git to use the editor. To do this, open a command prompt and type `git config --global core.editor <editor>`. Replace `<editor>` with the name of the editor you installed, such as `atom.exe` or `subl.exe`.

4. **Test Setup**

Once you have configured Git with your editor, you can test the setup by running the command `git commit`. This will open the editor you specified and you can write your commit message. Once you save and close the editor, the commit will be created.
