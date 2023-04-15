---
title: Copy changes from a specific commit to the working copy without committing them
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: It is not possible to cherry-pick changes to a working copy without committing them.
---

**Contents**

[TOC]

### Definition
Cherry-picking is a Git feature that allows you to choose a commit from one branch and apply it to another. This allows you to selectively pull changes from one branch into another, without having to merge the two branches together.

### Cherry-Pick to Working Copy
When cherry-picking to a working copy, the changes from the chosen commit are applied directly to the working tree, without creating a new commit. This allows you to test out the changes before committing them to the branch.

### Benefits
Cherry-picking to a working copy can be useful when you need to test out changes before committing them. It also allows you to quickly apply changes to your working tree without having to switch branches or create a new commit.

### How To
To cherry-pick to a working copy, use the `git cherry-pick <commit>` command, where `<commit>` is the commit hash of the commit you want to cherry-pick. This will apply the changes from the chosen commit to your working tree, without creating a new commit.
