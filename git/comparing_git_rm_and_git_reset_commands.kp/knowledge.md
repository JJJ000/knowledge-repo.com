---
title: "git rm --cached x" removes x from the staging area but keeps it in the working directory, while "git reset head -- x" removes x from the staging area and reverts it to the version in the last commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: `git rm --cached x` removes the file from the staging area and the repository, while `git reset head -- x` only removes the file from the staging area.
---

**Contents**

[TOC]

### git rm --cached x

`git rm --cached x` removes the file `x` from the staging area, but leaves the file in the working directory. This command is useful when you want to unstage a file that has already been staged.

### git reset head -- x

`git reset head -- x` removes the file `x` from the staging area and also removes the changes to the file from the working directory. This command is useful when you want to discard changes to a file that has already been staged.
