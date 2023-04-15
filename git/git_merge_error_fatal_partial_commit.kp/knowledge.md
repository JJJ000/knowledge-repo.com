---
title: Error encountered when attempting to commit after a merge - fatal cannot perform a partial commit while merging
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You must commit all merged changes together, so you cannot do a partial commit during a merge.
---

**Contents**

[TOC]

### Overview
When trying to commit after a merge, it is possible to encounter a Git error message stating "fatal: cannot do a partial commit during a merge". This error occurs when attempting to commit a merge without first resolving any conflicts between the files.

### Cause
This error occurs when a merge is attempted without first resolving any conflicts between the files. When merging two branches, Git will attempt to automatically merge the differences between the two branches. If there are any conflicts, Git will not be able to complete the merge and will display this error.

### Resolution
To resolve this error, the user must first resolve any conflicts between the files. This can be done by manually editing the files to resolve the conflicts, or by using a merge tool such as Meld or KDiff3. Once the conflicts have been resolved, the user can then commit the merge.
