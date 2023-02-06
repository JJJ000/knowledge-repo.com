---
title: How to undo commits in a pull request
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To remove commits from a pull request in Git, use the `git revert` command.
---

**Contents**

[TOC]

# Section 1: Create a New Branch
1. Checkout the branch you want to remove commits from
2. Create a new branch off of the branch you want to remove commits from

# Section 2: Reset the Branch
1. Reset the branch to the commit before the commits you want to remove
2. Checkout the branch you created in Section 1

# Section 3: Rebase the Branch
1. Rebase the branch you created in Section 1 onto the branch you reset in Section 2

# Section 4: Push the Branch
1. Push the branch with the commits removed to the remote repository
