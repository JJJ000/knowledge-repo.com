---
title: Apply a specific version from the git stash
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: git stash apply applies the most recently stashed changes to the current working directory.
---

**Contents**

[TOC]

### What is Stash Apply?

Stash apply is a Git command used to reapply changes that have been stashed away. This command is used to take the changes that were previously stored away and apply them back to the working directory.

### Syntax

The syntax for the stash apply command is as follows:

git stash apply [<stash>]

### Examples

To apply the most recent stash, you would use the following command:

git stash apply

To apply a specific stash, you would use the following command:

git stash apply <stash>

### Additional Information

It is important to note that the stash apply command does not remove the stashed changes from the stash list. In order to do that, you must use the git stash drop command. Additionally, it is also important to note that the stash apply command will only apply the changes that were stashed away, and not any changes that have been made to the working directory since the stash was created.
