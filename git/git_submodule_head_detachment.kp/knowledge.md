---
title: What is the reason for my git submodule head being disconnected from the master branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A Git submodule HEAD is detached from master when it is not pointing to the latest commit in the master branch of the submodule`s repository.
---

**Contents**

[TOC]

# Section 1: What is a Git Submodule?
A Git Submodule is a tool used to keep track of external code repositories within a larger project. It allows developers to link to and keep their project up-to-date with a remote repository.

# Section 2: What Does HEAD Detached From Master Mean?
When a Git Submodule is in a “HEAD detached from master” state, it means that the local version of the submodule is out of sync with the remote repository. This can happen when changes have been made to the submodule that have not been pushed to the remote repository yet.

# Section 3: How to Resolve a Detached HEAD
To resolve a detached HEAD, the changes made to the submodule must be committed and pushed to the remote repository. This will bring the local version of the submodule in line with the remote repository and the HEAD detached from master issue will be resolved.

# Section 4: Conclusion
Git Submodules are a useful tool for keeping track of external code repositories within a larger project. When the local version of the submodule is out of sync with the remote repository, the state of the submodule will be “HEAD detached from master”. To resolve this issue, the changes made to the submodule must be committed and pushed to the remote repository.
