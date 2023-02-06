---
title: How can I merge the first two commits in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git rebase -i HEAD~2` to combine the first two commits of a Git repository.
---

**Contents**

[TOC]

# Section 1: Preparing to Combine Commits

1. Checkout the repository and make sure you have the latest version of the code. 
2. Use `git log` command to view the commits and identify the two commits you want to combine. 
3. Use `git checkout` command to switch to the commit you want to combine.

# Section 2: Combining Commits

1. Use `git rebase -i` command to open the interactive rebase window. 
2. In the interactive rebase window, find the two commits you want to combine and replace the `pick` keyword with `squash` for one of the commits. 
3. Save and close the window.

# Section 3: Finalizing the Combination

1. Use `git commit --amend` to finalize the combination of the two commits. 
2. Push the changes to the remote repository.

# Section 4: Verifying the Combination

1. Use `git log` to view the commits and verify that the two commits have been combined.
