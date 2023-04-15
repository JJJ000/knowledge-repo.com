---
title: How to combine multiple commits into one on a git branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git rebase -i HEAD~<number of commits>`, replacing <number of commits> with the number of commits to be squashed.
---

**Contents**

[TOC]

### Using `rebase`
1. Checkout the branch you want to squash the commits on.
2. Run `git rebase -i HEAD~<number_of_commits_to_squash>`. This will open an editor showing all the commits that will be squashed.
3. Replace `pick` with `squash` for all the commits you want to squash.
4. Save and close the editor.
5. Push the branch to the remote repository.

### Using `merge`
1. Checkout the branch you want to squash the commits on.
2. Merge the branch with the branch you want to squash the commits into.
3. Push the branch to the remote repository.
