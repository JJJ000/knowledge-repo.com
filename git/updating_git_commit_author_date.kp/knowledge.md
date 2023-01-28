---
title: Change the author date of a git commit when making modifications
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, the author date of a git commit cannot be changed when amending.
---

**Contents**

[TOC]

### Yes

When amending a git commit, it is possible to update the author date. This can be done using the `--date` option when running the `git commit --amend` command. For example, to update the author date to the current date and time, you could run the command `git commit --amend --date="$(date)"`.

### No

It is also possible to amend a git commit without updating the author date. This can be done by running the `git commit --amend` command without any additional options. In this case, the author date will remain the same as the original commit.
