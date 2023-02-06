---
title: What is the process for combining multiple commits into a single patch using git format-patch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To squash commits into one patch with git format-patch, use the `--squash` option.
---

**Contents**

[TOC]

# Section 1: Prerequisites

Before you can squash commits into one patch with git format-patch, you must first have a repository with multiple commits.

# Section 2: Squash Commits

To squash multiple commits into one patch, you can use the command `git rebase -i <commit>`, where `<commit>` is the commit you want to start the rebase from. This command will open an interactive editor, where you can select the commits you want to squash.

# Section 3: Format Patch

Once you have finished squashing your commits, you can use the command `git format-patch <commit>..HEAD` to generate a patch file. This command will generate a patch file for all commits since `<commit>`.

# Section 4: Apply Patch

Finally, you can use the command `git am <patch-file>` to apply the patch file. This will apply the changes from the patch file to your repository.
