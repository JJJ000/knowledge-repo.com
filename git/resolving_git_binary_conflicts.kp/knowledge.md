---
title: Solving a git dispute involving binary files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: For binary files, the best option is to discard both versions and manually merge the files.
---

**Contents**

[TOC]

### Using a Merge Tool

Using a merge tool is the recommended approach for resolving conflicts with binary files. Merge tools are applications that allow you to compare two versions of a file and manually select which changes to keep and which changes to discard. Popular merge tools used with Git include KDiff3, Meld, and Beyond Compare.

### Resolving Manually

If a merge tool is not available, conflicts with binary files can be resolved manually. This process involves manually comparing the two versions of the file to determine which changes should be kept and which should be discarded. Once the changes have been identified, the conflicting sections should be edited to include only the desired changes.

### Recording the Resolution

Once the conflict has been resolved, the resolution should be recorded in Git. This can be done by running the `git add` command to add the edited file to the staging area and then running the `git commit` command to commit the changes. This will allow the resolution to be tracked in the repository's commit history.

### Testing the Resolution

Finally, the resolution should be tested to ensure that the desired changes were included and that the file is functioning as expected. This can be done by running the file or testing it in the appropriate environment. Once the resolution has been tested and verified, the conflict can be considered resolved.
