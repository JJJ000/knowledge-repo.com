---
title: What is the correct procedure for changing the active branch in a bare git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In a bare repository, the active branch can be changed by setting the HEAD pointer to the desired branch.
---

**Contents**

[TOC]

# Section 1: Cloning the Repository
The first step in changing the active branch of a bare repository is to clone the repository to a local machine. This can be done using the `git clone` command.

# Section 2: Setting the Active Branch
Once the repository is cloned, the active branch can be set using the `git checkout` command. This command will set the active branch to the specified branch.

# Section 3: Pushing the Changes
Once the active branch is set, the changes can be pushed to the remote repository using the `git push` command.

# Section 4: Verifying the Changes
The last step is to verify that the changes have been successfully pushed to the remote repository. This can be done using the `git status` command, which will show the active branch and any changes that have been made.
