---
title: What should be excluded from the comments in .gitignore?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, comments should not be included in .gitignore.
---

**Contents**

[TOC]

### What is .gitignore?

.gitignore is a file in a git repository that specifies which files and directories should be ignored by git when performing operations such as commits and pushes.

### What Should be Included in .gitignore?

Files and directories that should not be tracked by git should be included in .gitignore. This typically includes files such as configuration files, compiled binaries, and temporary files.

### How to Comment in .gitignore

Comments in .gitignore are preceded by a hash (`#`) character. For example:

```git
### This is a comment
```

Comments can be used to explain why certain files and directories are being excluded from the repository.
