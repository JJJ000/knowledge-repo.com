---
title: Which commit contains this blob?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The commit that contains the blob can be found by using the git log command to search for the blob`s SHA-1 hash.
---

**Contents**

[TOC]

### Commit Hash

The commit hash for the blob can be found by running the command `git log --pretty=format:"%H" --name-only --full-diff <blob-id>`.

### Commit Message

The commit message associated with the commit can be found by running the command `git log --pretty=format:"%s" <commit-hash>`.
