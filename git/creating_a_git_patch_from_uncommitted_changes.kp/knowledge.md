---
title: Generate a git patch from the modifications that have not been committed in the present working directory
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git format-patch HEAD` to generate a git patch from the uncommitted changes in the current working directory.
---

**Contents**

[TOC]

`**` Generating the Patch**

1. Run the command `git diff > patch-file.patch` 
2. This will generate a patch file with the name `patch-file.patch`

`**` Applying the Patch**

1. Run the command `git apply patch-file.patch`
2. This will apply the patch to the current working directory

`**` Verifying the Patch**

1. Run the command `git diff --staged`
2. This will show the changes that were applied by the patch

`**` Committing the Patch**

1. Run the command `git commit -m "Applied patch-file.patch"`
2. This will commit the patch to the current branch
