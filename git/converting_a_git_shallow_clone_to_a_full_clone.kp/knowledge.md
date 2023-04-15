---
title: What is the process for changing a git shallow clone to a full clone?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git fetch --unshallow` in the shallow clone to convert it to a full clone.
---

**Contents**

[TOC]

### Prerequisites

Before attempting to convert a shallow clone to a full clone, you should ensure that you have the following:

- A local Git repository with a shallow clone of the remote repository
- Access to the remote repository

### Configure Git

To convert a shallow clone to a full clone, you must configure Git to fetch the entire history of the repository. This can be done by running the following command in the local repository:

```git
git config --local --add remote.origin.fetch "+refs/heads/*:refs/remotes/origin/*"
```

### Fetch Data

Once the configuration is complete, you must fetch the entire history of the remote repository. This can be done by running the following command in the local repository:

```git
git fetch --unshallow
```

### Verify

To verify that the shallow clone has been converted to a full clone, run the following command in the local repository:

```git
git rev-list --count HEAD
```

This will output the total number of commits in the repository. If the number is greater than the number of commits that were included in the shallow clone, then the conversion was successful.
