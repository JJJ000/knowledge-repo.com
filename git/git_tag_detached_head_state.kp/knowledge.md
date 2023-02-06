---
title: Exploring a git tag can result in a "detached head state"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A detached HEAD state occurs when you check out a Git tag, meaning that you are no longer on the branch that the tag is associated with.
---

**Contents**

[TOC]

# What is a Git Tag?
A Git tag is a label that is used to mark a specific version of a repository. It is used to track changes and provide an easy way to identify and refer to a particular version of a repository.

# What is a Detached HEAD State?
A detached HEAD state is a state in Git where the HEAD pointer is not pointing to the branch or commit that is currently checked out. This means that any changes made in this state are not tracked in the repository and will not be included in future commits.

# How Does Checking Out a Git Tag Lead to a Detached HEAD State?
When a Git tag is checked out, the HEAD pointer is moved from the branch or commit that was previously checked out to the commit that is associated with the tag. This causes the HEAD pointer to become detached from the branch or commit that was previously checked out, thus entering a detached HEAD state.

# What Can Be Done About a Detached HEAD State?
If changes are made while in a detached HEAD state, they can be committed and then a new branch can be created from the commit. This will allow the changes to be tracked in the repository. Additionally, the HEAD pointer can be moved back to the branch or commit that was previously checked out.
