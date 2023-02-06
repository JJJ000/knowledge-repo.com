---
title: Move the ~ directory to a different location in a windows install of git bash
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The location of the ~ directory in a Windows install of Git Bash cannot be changed.
---

**Contents**

[TOC]

1. Find the Current Location of the ~ Directory

In Git Bash, type the command `echo $HOME` and press enter. This will display the current location of the ~ directory.

2. Change the Location of the ~ Directory

To change the location of the ~ directory, open the file `.bashrc` in a text editor. This file can be found in the same directory as the `.gitconfig` file.

3. Edit the .bashrc File

In the `.bashrc` file, find the line that reads `export HOME=` and change the path after the equals sign to the new location of the ~ directory.

4. Save and Reload the .bashrc File

Save the `.bashrc` file and then type the command `source .bashrc` in Git Bash to reload the file. The ~ directory is now changed to the new location.
