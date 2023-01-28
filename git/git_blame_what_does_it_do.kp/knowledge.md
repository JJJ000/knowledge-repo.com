---
title: What is the purpose of the 'git blame' command?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git blame shows the author of each line in a file, as well as the last commit that modified each line.
---

**Contents**

[TOC]

### What it Does

Git blame is a command that displays information about the author of each line in a file. It shows the author, the commit ID, and the date of the most recent commit for each line in the file. 

### How it Works

Git blame looks at the history of a file and finds the most recent commit for each line. It then displays the author, the commit ID, and the date of the commit. 

### Benefits

Git blame can be used to quickly identify who made changes to a file and when they were made. This can be useful for debugging or tracking down the source of a bug. 

### Limitations

Git blame only shows information about the most recent commit for each line. It does not show any information about previous commits or changes made to the file. Additionally, it does not show any information about the changes made in the commit, only the author and date.
