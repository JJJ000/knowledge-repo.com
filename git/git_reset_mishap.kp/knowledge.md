---
title: Changes not committed to the repository remaining after a git reset --hard command
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, there are no unstaged changes left after git reset --hard.
---

**Contents**

[TOC]

**Unstaged Changes Left in Working Directory**

When a git reset --hard command is executed, it will reset the HEAD pointer and the staging area to the most recent commit. This means that any changes that were made in the working directory will remain, as they are not part of the commit history.

**Staged Changes Left in Index**

Any changes that were staged in the index will remain after a git reset --hard command. This is because the command only affects the HEAD pointer and the staging area, and not the index. 

**Uncommitted Changes Left in Working Directory**

Any changes that were made in the working directory but not committed will remain after a git reset --hard command. This is because the command only affects the HEAD pointer and the staging area, and not the working directory.

**Untracked Changes Left in Working Directory**

Any untracked changes in the working directory will remain after a git reset --hard command. This is because the command only affects the HEAD pointer and the staging area, and not the working directory.
