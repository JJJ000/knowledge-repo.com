---
title: What are the distinctions between the git reset options of --mixed, --soft, and --hard?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git reset --mixed resets the index and working directory, --soft resets the index but leaves changes in the working directory, and --hard resets the index, working directory, and all changes made since the last commit.
---

**Contents**

[TOC]

### Git Reset --mixed
Git reset --mixed is the default option when running the git reset command. It resets the HEAD to the specified state, but keeps the index and working directory intact. This means that any changes made to the files in the working directory will not be lost.

### Git Reset --soft
Git reset --soft resets the HEAD to the specified state, but keeps the index and working directory changes intact. This means that any changes made to the files in the working directory will not be lost, but they will not be committed.

### Git Reset --hard
Git reset --hard resets the HEAD, index, and working directory to the specified state. This means that any changes made to the files in the working directory will be lost and all changes will be discarded.
