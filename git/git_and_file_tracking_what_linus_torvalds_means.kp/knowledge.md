---
title: What is linus torvalds implying when he states that git never keeps track of a file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git never stores any information about a file`s content or history, only its current state.
---

**Contents**

[TOC]

### Definition

Git is a version control system (VCS) for tracking changes in computer files and coordinating work on those files among multiple people.

### Meaning

Linus Torvalds is referring to the fact that Git does not track files in the same way as other version control systems. Instead, Git stores a snapshot of the entire repository every time a commit is made. This means that it is not necessary to track individual files, as the repository as a whole is tracked. This makes it easier to work with large repositories, as only changes to the repository are tracked, rather than individual files.
