---
title: How can I make "git pull" replace my local files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `--force` or `-f` flag with `git pull` to force overwrite local files.
---

**Contents**

[TOC]

### 1. Checkout Local Branch
First, you need to checkout the local branch you want to overwrite. To do this, you can use the following command:

```shell
git checkout <branch_name>
```

### 2. Force Pull
Next, you can use the `--force` flag to force the pull. This will overwrite any local changes with the changes from the remote repository. The command for this is:

```shell
git pull --force
```

### 3. Discard Local Changes
Finally, if you want to discard any local changes that were made, you can use the `--discard-changes` flag. This will discard any local changes and replace them with the changes from the remote repository. The command for this is:

```shell
git pull --force --discard-changes
```
