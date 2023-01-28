---
title: What is the procedure for determining the amount of lines altered between two commits in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the `git diff` command to calculate the number of lines changed between two commits.
---

**Contents**

[TOC]

### Using Git Log

Using the `git log` command, you can compare the two commits and see the number of lines changed between them. To do this, you must first find the commit hashes of the two commits you want to compare. To find the commit hashes, use the `git log` command with the `--oneline` option.

### Using Git Diff

Once you have the commit hashes, you can use the `git diff` command to compare the two commits and see the number of lines changed. To do this, run the `git diff` command with the two commit hashes as arguments. This will output the differences between the two commits, including the number of lines changed.

### Counting the Output

In the output of the `git diff` command, the number of lines changed is indicated by the number of lines beginning with a '+' or a '-'. To count the number of lines changed, simply count the number of lines beginning with either a '+' or a '-'.

### Other Options

Git also provides several other options for counting the number of lines changed between two commits. For example, the `git diff --stat` command will output a summary of the changes between the two commits, including the number of lines changed. Additionally, the `git blame` command can be used to count the number of lines changed in a single commit.
