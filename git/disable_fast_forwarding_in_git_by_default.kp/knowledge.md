---
title: Is it possible to set fast forwarding to be disabled by default in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, fast forwarding cannot be disabled by default in git.
---

**Contents**

[TOC]

1. Overview 
2. How to Make Fast-Forwarding Off by Default in Git

### Overview 
Git is a version control system (VCS) used for tracking changes in computer files and coordinating work on those files among multiple people. It is an open-source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. By default, git allows for fast-forwarding, which is a mode of merging that moves all branches forward to the same commit. This can be beneficial when merging branches, as it eliminates unnecessary commits and makes the history easier to read. However, it can also lead to unexpected behavior, and it can be beneficial to turn off fast-forwarding in some cases. 

### How to Make Fast-Forwarding Off by Default in Git
The easiest way to make fast-forwarding off by default is to set the `merge.ff` configuration option to `false`. This can be done by running the following command:

```git
git config --global merge.ff false
```

This will make the fast-forwarding option off by default for all repositories on the system. However, if you only want to change the setting for a single repository, you can run the command within that repository instead.

Once the setting is changed, it will apply to all future merges. If you want to turn off fast-forwarding for an existing merge, you can use the `--no-ff` flag when running the merge command.

By making fast-forwarding off by default, you can ensure that all merges are performed in a consistent manner, and that unexpected behavior is avoided.
