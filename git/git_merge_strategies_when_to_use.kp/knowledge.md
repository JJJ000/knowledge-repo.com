---
title: What are the different scenarios in which you would use different git merge strategies?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: For fast-forward merges, use when the branch being merged in is ahead of the current branch; for recursive merges, use when the two branches have diverged; for squash merges, use when combining multiple commits into one; and for rebase merges, use when wanting to keep a linear history.
---

**Contents**

[TOC]

1. Fast-Forward Merge: 
This is the default merge strategy used by Git. It is used when merging a commit that is a direct ancestor of the current commit. This is the simplest and most common merge strategy, and it results in a linear history.

2. Recursive Merge: 
This is the most common merge strategy used by Git. It is used when merging two branches that have diverged. It will combine the changes from both branches, and it will create a new merge commit if there are any conflicts.

3. Octopus Merge: 
This is a less common merge strategy used by Git. It is used when merging more than two branches at once. It will combine the changes from all of the branches, and it will create a new merge commit if there are any conflicts.

4. Resolve Merge: 
This is the least common merge strategy used by Git. It is used when merging two branches that have diverged, but the recursive merge strategy is unable to successfully merge the branches. This merge strategy requires manual intervention to resolve any conflicts.
