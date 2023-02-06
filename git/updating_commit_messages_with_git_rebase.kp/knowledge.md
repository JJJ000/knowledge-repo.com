---
title: Edit an existing commit message using "git rebase"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git rebase -i` to interactively change the commit message of any commit in the current branch.
---

**Contents**

[TOC]

### Step 1: Check Out the Commit You Want to Change

Using `git rebase`, you can check out the commit you want to change by running the following command:

```
git rebase -i <commit-ID>
```

Replace `<commit-ID>` with the hash of the commit you want to change. This will open up an interactive rebase window.

### Step 2: Change the Commit Message

In the interactive rebase window, locate the commit you want to change and replace the word `pick` with `reword`. This will allow you to change the commit message.

### Step 3: Save and Exit

Once you have changed the commit message, save and exit the interactive rebase window. This will open up a new window where you can enter the new commit message.

### Step 4: Continue Rebase

After you have entered the new commit message, continue the rebase process by running the following command:

```
git rebase --continue
```

This will apply the new commit message to the commit you wanted to change.
