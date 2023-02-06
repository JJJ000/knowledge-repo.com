---
title: How to cancel a git rebase while using vim during interactive editing
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Press Esc followed by q! to abort the git rebase from inside vim.
---

**Contents**

[TOC]

# Section 1: Exit Vim

1. Press the `Esc` key to enter command mode.
2. Type `:q!` to quit Vim without saving.

# Section 2: Abort the Rebase

1. After exiting Vim, type `git rebase --abort` to abort the rebase.

# Section 3: Confirm the Abort

1. Type `git status` to confirm that the rebase has been aborted.

# Section 4: Reset the Branch

1. Type `git reset --hard HEAD` to reset the branch to its original state.
