---
title: Replace the local version of the files with the version from the remote repository using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git fetch` followed by `git reset --hard origin/master`.
---

**Contents**

[TOC]

# Section 1: Fetch the Remote Version
1. Open the command line and navigate to the local repository.
2. Run the command `git fetch origin`.

# Section 2: Discard Local Changes
1. Run the command `git reset --hard origin/master`.

# Section 3: Pull the Remote Version
1. Run the command `git pull origin master`.

# Section 4: Verify the Changes
1. Run the command `git status` to verify that the local repository is now in sync with the remote version.
