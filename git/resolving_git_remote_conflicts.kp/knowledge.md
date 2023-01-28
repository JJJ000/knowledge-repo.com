---
title: When pulling from a git remote, use remote changes to address any conflicts
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Merge the remote changes with your local changes using a merge strategy such as `recursive` or `ours`.
---

**Contents**

[TOC]

### Identifying Conflicts

When pulling from a Git remote, conflicts can arise if the same file has been changed by two different users. When this occurs, the Git client will inform the user that there are conflicts that need to be resolved.

### Resolving Conflicts

The first step in resolving conflicts is to identify which of the remote changes should be kept and which should be discarded. This can be done by comparing the local and remote versions of the file and deciding which changes should be kept.

### Merging Changes

Once the desired changes have been identified, the next step is to merge the changes into a single version of the file. This can be done manually or with a merge tool such as GitKraken.

### Committing Changes

Once the conflicts have been resolved, the changes can be committed to the local repository. This will allow the user to push the changes to the remote repository and ensure that all changes are up to date.
