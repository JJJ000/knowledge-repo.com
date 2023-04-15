---
title: Can I safely shallow clone with --depth 1, create commits, and pull updates again?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, it is safe to shallow clone with --depth 1, create commits, and pull updates again in Git.
---

**Contents**

[TOC]

### Yes
Shallow cloning with --depth 1 is a safe and efficient way to work with a Git repository. When a shallow clone is created, only the latest commit is downloaded from the remote repository. This reduces the amount of data that needs to be transferred, making it faster and more efficient. Additionally, any commits made in a shallow clone are stored locally, so they are not affected by any updates pulled from the remote repository.

### Commits
Commits made in a shallow clone have the same effect as commits made in a standard clone. They are stored locally and can be pushed to the remote repository. The only difference is that the commits are not stored in the remote repository until they are pushed.

### Pull Updates
Pulling updates from the remote repository in a shallow clone is also safe. The updates are only applied to the latest commit, so any local commits are not affected. Additionally, any new commits from the remote repository are downloaded and stored locally, so they can be pushed to the remote repository at a later time.

### Conclusion
Shallow cloning with --depth 1 is a safe and efficient way to work with a Git repository. Commits made in a shallow clone are stored locally and can be pushed to the remote repository, and pulling updates from the remote repository does not affect any local commits.
