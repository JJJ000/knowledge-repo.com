---
title: Committing changes with no content to the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, it is not possible to push empty commits to a remote in Git.
---

**Contents**

[TOC]

### What is an Empty Commit?
An empty commit is a commit that contains no changes to the repository. It can be created by simply adding a commit message without making any changes.

### Why Push Empty Commits?
Empty commits can be useful in certain situations, such as when trying to fix a broken build or when wanting to create a commit to mark a certain point in time. They can also be used to quickly commit changes that are too small to be worth the effort of committing individually.

### How to Push Empty Commits
To push an empty commit to a remote repository, use the `git commit --allow-empty` command. This command will create an empty commit with the specified commit message.

### Conclusion
Empty commits can be useful in certain situations and are easy to create and push to a remote repository. However, it is important to consider the implications of creating an empty commit, as it can lead to confusion and may not be the best solution for a given situation.
