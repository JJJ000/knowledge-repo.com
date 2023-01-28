---
title: Perform a git pull in all subfolders
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, git pull only works in the current directory.
---

**Contents**

[TOC]

### Using Bash
1. Create a script to run the command in all subdirectories:

```bash
###!/bin/bash

### loop through all subdirectories
for dir in */; do
    # navigate to the directory
    cd "$dir"
    # run the command
    git pull
    # navigate back to the parent directory
    cd ..
done
```

2. Execute the script:

```bash
sh script.sh
```

### Using Find
1. Create a script to run the command in all subdirectories:

```bash
###!/bin/bash

### set the directory to search
DIR="."

### loop through all subdirectories
find $DIR -type d -exec bash -c "cd '{}' && git pull" \;
```

2. Execute the script:

```bash
sh script.sh
```
