---
title: How can I reset the origin/master branch to a specific commit using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To reset origin/master to a commit, use the command `git reset --hard <commit-hash>`.
---

**Contents**

[TOC]

### Step 1: Checkout the Commit

You can reset `origin/master` to a specific commit by first checking out the commit. This can be done using the `git checkout` command.

Syntax:

```
git checkout <commit>
```

### Step 2: Reset Origin/Master

Once you have checked out the desired commit, you can reset `origin/master` to it by using the `git reset` command.

Syntax:

```
git reset --hard origin/master <commit>
```

### Step 3: Push the Commit

Finally, you can push the commit to `origin/master` by using the `git push` command.

Syntax:

```
git push origin/master <commit> --force
```

### Step 4: Verify the Reset

To verify the reset, you can use the `git log` command to check the history of `origin/master`.

Syntax:

```
git log origin/master
```
