---
title: What is the distinction between using ".." and "..." in git commit ranges?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Double-dot `..` is used to specify a range of commits that excludes the commits on the boundary, while triple-dot `...` is used to specify a range of commits that includes the commits on the boundary.
---

**Contents**

[TOC]

### Double-dot ".." 
The double-dot ".." operator is used to specify a range of commits that includes all commits between two specified commits, including the specified commits.

### Triple-dot "..."
The triple-dot "..." operator is used to specify a range of commits that includes all commits between two specified commits, but excludes the specified commits.
