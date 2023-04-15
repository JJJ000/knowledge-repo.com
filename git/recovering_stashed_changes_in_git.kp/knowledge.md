---
title: What is the process for retrieving uncommitted changes that have been stashed?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git stash pop` to recover stashed uncommitted changes in Git.
---

**Contents**

[TOC]

### Find the Stash

The first step to recovering stashed uncommitted changes in Git is to find the stash. To do this, run the following command:

`git stash list`

This will show a list of all the stashes that have been created.

### Apply the Stash

Once you have identified the stash that you want to recover, you can apply it using the following command:

`git stash apply <stash_id>`

Where <stash_id> is the identifier of the stash you want to recover.

### Remove the Stash

Once you have applied the stash, you can remove it using the following command:

`git stash drop <stash_id>`

Where <stash_id> is the identifier of the stash you want to remove.

### Commit the Changes

Finally, you can commit the changes that you have recovered from the stash using the following command:

`git commit -m "Your commit message"`
