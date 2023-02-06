---
title: How to configure visual studio code as the default git mergetool, including for 3-way merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Set the `merge.tool` and `mergetool.<tool>.cmd` configuration settings to `code --wait` in the Git configuration file.
---

**Contents**

[TOC]

# Section 1: Setting up Visual Studio Code as Default Editor

1. First, open up the terminal and type in `git config --global core.editor "code --wait"`
2. This will set Visual Studio Code as the default editor for Git MergeTool.

# Section 2: Configuring Visual Studio Code for 3-way Merging

1. Open up Visual Studio Code and go to `File > Preferences > Settings`
2. In the search bar, type in `git.autofetch` and set it to `true`
3. This will enable Visual Studio Code to automatically fetch changes from the remote repository when merging.

# Section 3: Using Visual Studio Code for 3-way Merge

1. To start the 3-way merge, open up the terminal and type in `git merge --no-edit`
2. This will open up Visual Studio Code with the 3-way merge view
3. From here, you can select which changes you want to keep and discard.

# Section 4: Finishing the Merge

1. After selecting the desired changes, click on the `Commit` button
2. This will finish the 3-way merge and the changes will be pushed to the remote repository.
