---
title: What are the steps to display uncommitted changes in git, and how can one explain git diffs in depth?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To view uncommitted changes in Git, use the `git diff` command to show differences between commits, branches, and files.
---

**Contents**

[TOC]

### Showing Uncommitted Changes

Git provides several methods for viewing changes that have not yet been committed to the repository.

### git status

The `git status` command can be used to view all of the changes that have been made to the working tree since the last commit. This command will display a list of all modified or untracked files, as well as any staged changes that are ready to be committed.

### git diff

The `git diff` command can be used to view the differences between two versions of a file. This command can be used to compare the working tree with the most recent commit, or to compare two commits.

### git diff --cached

The `git diff --cached` command can be used to view the differences between the staged changes and the most recent commit. This command is useful for reviewing changes before committing them to the repository.

### git difftool

The `git difftool` command can be used to view the differences between two versions of a file in a visual diff tool. This command is useful for making more detailed comparisons between two versions of a file.
