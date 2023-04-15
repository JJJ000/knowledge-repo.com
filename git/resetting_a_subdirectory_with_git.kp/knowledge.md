---
title: How can I use git reset --hard on a subdirectory?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You cannot git reset --hard a subdirectory; you can only reset the entire repository.
---

**Contents**

[TOC]

### Navigate to Subdirectory

Before you can reset the subdirectory, you need to navigate to it. To do this, you can use the `cd` command.

```
cd <subdirectory>
```

### Reset Subdirectory

Once you have navigated to the subdirectory, you can reset it using the `git reset --hard` command.

```
git reset --hard
```

### Verify Reset

To verify that the reset was successful, you can use the `git status` command.

```
git status
```

### Push Changes

Finally, you can push the changes to the remote repository using the `git push` command.

```
git push
```
