---
title: What is the method for determining if one commit is a descendant of another commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git merge-base` command to determine if one commit is a descendant of another commit.
---

**Contents**

[TOC]

# Using git log

Git log is a powerful tool that can be used to view the commit history of a repository. To determine if a commit is a descendant of another commit, you can use the `--ancestry-path` option in git log. This option will display all commits that are descendants of the specified commit.

# Syntax

The syntax for using the `--ancestry-path` option is as follows:

`git log --ancestry-path <commit>..<commit>`

This will display all commits that are descendants of the first commit and ancestors of the second commit.

# Example

For example, to determine if commit `f2d2f8` is a descendant of commit `d6b1a2`, you would run the following command:

`git log --ancestry-path d6b1a2..f2d2f8`

This will display all commits that are descendants of `d6b1a2` and ancestors of `f2d2f8`. If `f2d2f8` is listed in the output, then it is a descendant of `d6b1a2`.
