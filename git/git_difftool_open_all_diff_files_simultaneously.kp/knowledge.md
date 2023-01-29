---
title: Open all diff files with git difftool simultaneously, rather than one at a time
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, difftool can only open diff files one at a time.
---

**Contents**

[TOC]

### Using Bash Script

A bash script can be used to open all diff files immediately in difftool. The script can be written to loop through all diff files and open them in difftool.

### Syntax

The syntax for the script will be as follows:

```git
###!/bin/bash

for file in $(git difftool --dir-diff); do
  git difftool $file
done
```

### Execution

The script can be executed by running the following command in the terminal:

```git
bash script.sh
```

### Output

The output of the script will be the opening of all diff files in difftool immediately, without having to open them in serial.
