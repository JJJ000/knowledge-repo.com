---
title: It is not possible to commit because there are still files that have not been merged into the git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You must resolve all unmerged files before committing changes.
---

**Contents**

[TOC]

# Overview

When attempting to commit changes to a Git repository, an error message may appear stating "commit is not possible because you have unmerged files". This error is caused by a merge conflict, which occurs when two branches of the repository have changes to the same line of the same file. In order to commit the changes, the merge conflict must first be resolved.

# Causes of Merge Conflicts

Merge conflicts can occur when two branches of the repository have changes to the same line of the same file. This can happen when two developers are making changes to the same file in different branches, and one of the developers attempts to merge their changes into the other branch.

# Resolving Merge Conflicts

Merge conflicts can be resolved by manually editing the file to combine the changes from both branches. This can be done by opening the file in a text editor and manually combining the changes from both branches. Once the changes have been combined, the file can be committed to the repository.

# Conclusion

Merge conflicts can occur when two branches of a repository have changes to the same line of the same file. In order to commit the changes, the merge conflict must be resolved by manually editing the file to combine the changes from both branches. Once the changes have been combined, the file can be committed to the repository.
