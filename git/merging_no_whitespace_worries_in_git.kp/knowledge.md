---
title: Combining without whitespace issues
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git can automatically merge changes without whitespace conflicts if the changes are on different lines.
---

**Contents**

[TOC]

# Section 1: Prerequisites
Before attempting to merge two branches without whitespace conflicts, it is important to ensure that both branches are in a clean state. This means that any changes that have been made to either branch should be committed and pushed to the remote repository before attempting to merge them. Additionally, any changes that have been made to either branch should be reviewed to ensure that they are valid and do not introduce any whitespace conflicts.

# Section 2: Merge
Once the branches are in a clean state, the merge process can begin. To merge two branches without whitespace conflicts, the `--no-whitespace` flag should be used when merging. This flag will tell Git to ignore any whitespace conflicts that may arise when merging the two branches.

# Section 3: Resolve Conflicts
In the event that a whitespace conflict is encountered during the merge process, it can be resolved by manually editing the conflicting files. This can be done by opening the conflicting files in an editor and manually resolving the conflict by deleting or changing the whitespace that is causing the conflict.

# Section 4: Commit
Once the whitespace conflicts have been resolved, the changes should be committed and pushed to the remote repository. This will ensure that the changes are saved and can be used by other developers.
