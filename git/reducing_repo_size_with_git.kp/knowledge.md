---
title: Decrease the size of the git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git gc --aggressive` to reduce the size of the git repository.
---

**Contents**

[TOC]

#1. Remove Large Files

One way to reduce the size of a git repository is to remove large files that are no longer needed. This can be done by running the following command:

```git filter-branch --index-filter 'git rm --cached --ignore-unmatch <file-name>' --prune-empty -- --all```

This will remove the specified file from the repository and all previous commits.

#2. Remove Unnecessary Branches

Another way to reduce the size of a git repository is to remove unnecessary branches. This can be done by running the following command:

```git branch -d <branch-name>```

This will delete the specified branch from the repository.

#3. Compress Pack File

Git stores all the data in a pack file, which can be compressed to reduce the size of the repository. This can be done by running the following command:

```git gc --aggressive --prune=now```

This will compress the pack file and reduce the size of the repository.

#4. Prune Refs

Finally, git stores references to all the commits in the repository. These references can be pruned to reduce the size of the repository. This can be done by running the following command:

```git reflog expire --expire=now --all && git gc --prune=now --aggressive```

This will prune the references and reduce the size of the repository.
