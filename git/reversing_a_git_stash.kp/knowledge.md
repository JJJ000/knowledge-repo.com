---
title: Revert a git stash
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git stash pop` to undo a git stash.
---

**Contents**

[TOC]

**1. Check What Was Stashed**

Before you undo a git stash, it is important to check what was stashed. This can be done by running `git stash list` which will show a list of the stashes that have been saved.

**2. Apply the Stash**

Once you have identified the stash you want to undo, you can apply it by running `git stash apply <stash_name>` where `<stash_name>` is the name of the stash you want to apply. This will apply the stash to your current working directory.

**3. Remove the Stash**

Once you have applied the stash, you can remove the stash from the list of stashes by running `git stash drop <stash_name>` where `<stash_name>` is the name of the stash you want to remove.

**4. Commit the Changes**

Finally, you can commit the changes that were applied when you applied the stash by running `git commit -m "Your commit message here"`. This will commit the changes and undo the git stash.
