---
title: Merging multiple commits together before pushing to a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git rebase` command to combine multiple commits before pushing.
---

**Contents**

[TOC]

### Interactive Rebase

Interactive rebase is a useful tool for combining multiple commits before pushing in Git. This can be done by running the command ```git rebase -i <commit_id>```, where ```<commit_id>``` is the ID of the commit that is the starting point for the rebase. This will open up an editor with a list of all the commits from the starting point to the current HEAD.

### Reordering Commits

The commits can be reordered by simply moving the lines of the commits around. This is useful for grouping related commits together and creating a more logical commit history.

### Squashing Commits

Commits can also be squashed together by changing the word ```pick``` to ```squash``` on the lines of the commits that need to be combined. This will combine the commit messages into one and create a single commit out of multiple commits.

### Finishing the Rebase

Once the commits have been reordered and/or squashed, the interactive rebase can be finished by saving and exiting the editor. This will complete the rebase and the combined commits will now be ready to be pushed.
