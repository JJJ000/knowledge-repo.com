---
title: Compare the changes in a git repository to a stored stash
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can view the differences between a stash and the current state of your repository by running the command `git diff <stash>`.
---

**Contents**

[TOC]

### Overview

Git diff can be used to compare the differences between a stash and a commit. This comparison can be done in a few simple steps.

### Steps

1. Create a stash of the current changes by running `git stash`.
2. Make the desired changes to the code.
3. Run `git diff stash@{0}` to compare the changes between the current commit and the stash.
4. Review the differences and make any necessary changes.

### Conclusion

By using the `git diff` command, it is possible to compare the changes between a stash and a commit. This can be a useful tool for ensuring that the changes made to the code are correct before committing them.
