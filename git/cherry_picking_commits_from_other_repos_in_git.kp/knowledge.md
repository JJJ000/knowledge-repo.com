---
title: Can you select a commit from another git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Yes, it is possible to cherry-pick a commit from another git repository by using the `git cherry-pick` command.
---

**Contents**

[TOC]

Yes, it is possible to cherry-pick a commit from another git repository. 

### Prerequisites 

In order to cherry-pick a commit from another repository, the two repositories must be connected. This can be done by adding a remote URL to the repository that the commit is being cherry-picked from. This can be done using the `git remote add` command.

### Cherry-picking a Commit

Once the two repositories are connected, the commit can be cherry-picked using the `git cherry-pick` command. This command takes the SHA of the commit that is to be cherry-picked as an argument. This will then create a new commit in the repository with the same changes as the commit being cherry-picked. 

### Conflicts

If there are conflicts between the two repositories, they must be resolved before the commit can be cherry-picked. This can be done by manually editing the conflicting files and then adding and committing the changes.
