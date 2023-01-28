---
title: What is the process for changing the color of the git console?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git config --global color.ui auto` command to color the Git console.
---

**Contents**

[TOC]

`**` Installing ColorLS**

1. Install the ColorLS gem:

`gem install colorls`

2. To ensure that ColorLS is available, type `colorls` in the command line.

`**` Configuring ColorLS**

1. Open the `.bash_profile` file located in your home directory using your text editor of choice.

2. Add the following line to the end of the file:

`eval "$(colorls --shell)"`

3. Save the file and restart the terminal.

`**` Using ColorLS**

1. To use ColorLS, simply type `ls` in the command line.

2. You should now see a colorful display of the files and folders in the current directory.

`**` Customizing ColorLS**

1. To customize the colors used by ColorLS, open the `~/.config/colorls/config.yaml` file in your text editor of choice.

2. Here you can change the colors used for different file types, as well as customize the display of the output.

3. Save the file and restart the terminal to see your changes.
