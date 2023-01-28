---
title: What is the reason that git uses fast-forward merges as the default option?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git performs fast-forward merges by default to keep the history of the repository linear and easy to follow.
---

**Contents**

[TOC]

### Advantages
1. Fast-forward merges are easy to understand and implement. This makes them the preferred choice for the default merge strategy.
2. Fast-forward merges are less likely to cause conflicts. Since the entire history is preserved, there is no need to resolve any conflicts.
3. Fast-forward merges are faster than other types of merges, as they do not require any complex calculations.

### Disadvantages
1. Fast-forward merges do not create a new commit. This makes it difficult to track the history of the project.
2. Fast-forward merges can lead to a cluttered history if not used carefully. It is easy to lose track of changes when multiple branches are merged into a single branch.
