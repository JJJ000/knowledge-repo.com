---
title: What is the procedure for undoing a local git commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To cancel a local git commit, use the command `git reset --hard HEAD~1`.
---

**Contents**

[TOC]

### Step 1: Undo the Last Commit

To undo the last commit, use the `git reset` command with the `--soft` option. This will move the HEAD pointer back to the previous commit and leave the changes from the latest commit in the working directory.

```
git reset --soft HEAD^
```

### Step 2: Discard the Changes

Once the last commit has been undone, the changes can be discarded by running the `git reset` command with the `--hard` option. This will discard all changes made since the last commit.

```
git reset --hard HEAD
```

### Step 3: Push the Changes

Finally, the changes must be pushed to the remote repository to make the cancellation of the commit official.

```
git push origin <branch-name>
```
