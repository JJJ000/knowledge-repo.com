---
title: Clone a git repository without the .git directory
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: It is not possible to clone a git repository without the .git directory.
---

**Contents**

[TOC]

**Solution 1**

#### Using `--depth` Option

This option can be used to create a shallow clone with a history truncated to the specified number of commits.

```
git clone --depth <depth> <repository>
```

**Solution 2**

#### Using `--no-single-branch` Option

This option can be used to clone only the history leading to the tip of a single branch, either specified by the --branch option or the primary branch remote’s HEAD points at.

```
git clone --no-single-branch <repository>
```
