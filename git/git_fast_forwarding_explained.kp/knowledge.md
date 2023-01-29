---
title: How does git fast-forwarding work?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git fast-forwarding is a process of automatically advancing the branch pointer to the most recent commit when merging or rebasing.
---

**Contents**

[TOC]

### Introduction 
Git fast-forwarding is a feature of the version control system Git that allows for a branch to be quickly merged into another branch. It is a method of merging two branches together that minimizes the amount of work needed to be done.

### How it Works
When a branch is fast-forwarded, the commits from the source branch are added to the destination branch in the order that they were created. This means that all of the commits from the source branch are added to the destination branch without any additional work. This is different from a regular merge, which requires the user to manually resolve any conflicts that arise from the two branches being merged together.

### Benefits
The main benefit of Git fast-forwarding is that it is much faster than a regular merge. This is because it requires less work to be done, as all of the commits from the source branch are added to the destination branch without any additional work. Additionally, fast-forwarding can help to keep the history of a project organized, as all of the commits from the source branch are added in the order in which they were created.

### Limitations
One of the main limitations of Git fast-forwarding is that it can only be used when the two branches are compatible. If the two branches have conflicting changes, then a regular merge must be used instead of fast-forwarding. Additionally, fast-forwarding can lead to a cluttered commit history, as all of the commits from the source branch are added to the destination branch in the order in which they were created.
