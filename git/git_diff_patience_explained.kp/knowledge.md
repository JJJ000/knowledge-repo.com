---
title: What does "git diff --patience" do?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git diff --patience is used to show the differences between files using a more efficient algorithm that is better at handling large files with many small changes.
---

**Contents**

[TOC]

# What is Git Diff?
Git diff is a command used to show the difference between two commits or two versions of a file. It can also be used to compare the working tree and the index.

# What is Patience?
Patience is an algorithm used by Git diff to compare files. It is designed to be more efficient than the traditional diff algorithm and is used to detect small, but significant changes in the code.

# What is Git Diff --Patience?
Git diff --patience is a command used to compare two commits or two versions of a file using the patience algorithm. This command can be used to detect small, but significant changes in the code.

# Benefits of Using Git Diff --Patience
Using the patience algorithm with Git diff can help to identify small, but important changes in the code. This can help to ensure that any changes made to the code are correctly tracked and documented. Additionally, using the patience algorithm can help to reduce the time it takes to compare two versions of a file.
