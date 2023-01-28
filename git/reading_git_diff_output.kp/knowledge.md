---
title: What does the output from git diff mean?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git diff shows the differences between two commits or files in a text format.
---

**Contents**

[TOC]

### Overview

Git diff is a command that allows you to view the differences between two versions of a file. It can be used to compare the differences between two commits, two branches, or two different files. The output of the command will show the differences between the two versions of the file, including any lines that were added, removed, or modified.

### Format

The output of the git diff command is formatted as a patch file. It will show the differences between the two versions of the file, with each line beginning with either a +, -, or a space character. A + indicates that a line has been added, a - indicates that a line has been removed, and a space indicates that a line has been modified.

### Syntax

The syntax for the git diff command is as follows:

git diff [options] <commit> <commit>

Where the <commit> arguments can be either a commit ID, branch name, or file path.

### Example

For example, the following command will compare the differences between two commits, with the first commit being the "master" branch and the second commit being the "dev" branch:

git diff master dev
