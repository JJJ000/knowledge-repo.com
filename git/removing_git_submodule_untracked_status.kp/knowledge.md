---
title: What is the best way to remove the untracked status of git submodules?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git submodule update --init --recursive` to initialize and clone all submodules.
---

**Contents**

[TOC]

# Section 1: Removing the Submodule
1. Navigate to the root directory of your Git repository.
2. Run the command `git submodule deinit path/to/submodule` to remove the submodule from the repository.

# Section 2: Removing the Submodule Reference
1. Run the command `git rm path/to/submodule` to remove the reference to the submodule from the repository.

# Section 3: Committing the Changes
1. Run the command `git commit -m "Removed submodule"` to commit the changes.

# Section 4: Removing the Submodule Files
1. Run the command `rm -rf path/to/submodule` to delete the submodule files from your repository.
