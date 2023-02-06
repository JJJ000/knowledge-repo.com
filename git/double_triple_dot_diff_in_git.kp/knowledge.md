---
title: What is the distinction between using double-dot ".." and triple-dot "..." when specifying a commit range in a git diff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Double-dot `..` specifies a range of commits that excludes the end commit, while triple-dot `...` specifies a range of commits that includes the end commit.
---

**Contents**

[TOC]

# Double-Dot
The double-dot (..) operator is used to select a range of commits that are reachable from the first commit, but not the second. This operator is inclusive, meaning that both the first and second commits will be included in the range.

# Triple-Dot
The triple-dot (...) operator is used to select a range of commits that are not reachable from the first commit, but are reachable from the second commit. This operator is exclusive, meaning that neither the first nor the second commits will be included in the range.
