---
title: Revert the changes made by "git add <dir>"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To undo `git add <dir>`, use `git reset <dir>`.
---

**Contents**

[TOC]

# Step 1: Discard All Changes

To undo a `git add <dir>` command, the first step is to discard all changes that were added to the staging area. To do this, use the `git reset` command with the `--mixed` option:

```
git reset --mixed
```

# Step 2: Unstage Files

The next step is to unstage the files that were added with the `git add <dir>` command. This can be done with the `git reset` command with the `HEAD` option:

```
git reset HEAD <dir>
```

# Step 3: Remove Files from Working Tree

The third step is to remove the files from the working tree. This can be done with the `git clean` command with the `-f` option:

```
git clean -f <dir>
```

# Step 4: Commit Changes

Finally, the changes should be committed to ensure that the undo process is complete. This can be done with the `git commit` command:

```
git commit -m "Undo git add <dir>"
```
