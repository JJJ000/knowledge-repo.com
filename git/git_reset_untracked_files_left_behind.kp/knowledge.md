---
title: Git reset --hard head does not delete untracked files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, git reset --hard HEAD removes all changes, including untracked files.
---

**Contents**

[TOC]

### Yes

When using `git reset --hard HEAD`, all changes to tracked files in the working tree since the last commit are reverted, and any staged changes are also discarded. This includes any untracked files that have been added to the working tree since the last commit.

### No

However, any untracked files that have not been added to the working tree since the last commit will remain in the working tree and will not be affected by the `git reset --hard HEAD` command. These files will still be present after the command is executed.
