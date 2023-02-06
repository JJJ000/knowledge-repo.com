---
title: Can I use "git status" to check only the modified files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, it is not possible to `git status` only modified files.
---

**Contents**

[TOC]

### Yes

1. Use the `-m` option: `git status -m`
2. This will only show files that are modified, but not staged.

### No

1. `git status` will not show only modified files.
2. It will show all files that are tracked (staged, modified, and unmodified) and untracked files.
