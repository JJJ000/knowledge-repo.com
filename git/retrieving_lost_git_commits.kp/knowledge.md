---
title: Obtain a record of all git commits, including the 'missing' ones
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the command `git reflog` to get a list of all git commits, including the `lost` ones.
---

**Contents**

[TOC]

1. Cloning a Repository

In order to get a list of all git commits, including the 'lost' ones, the first step is to clone the repository. This can be done through the command line using the `git clone` command. This will create a local copy of the remote repository on your machine.

2. Checking Out a Specific Commit

Once the repository has been cloned, the next step is to check out a specific commit. This can be done using the `git checkout` command followed by the commit hash. This will move the current HEAD of the repository to the specified commit.

3. Listing Commits

Once a specific commit has been checked out, the next step is to list all commits in the repository. This can be done using the `git log` command. This will list all commits in the repository, including the 'lost' ones.

4. Viewing the Contents of a Commit

Once the commits have been listed, the next step is to view the contents of a particular commit. This can be done using the `git show` command followed by the commit hash. This will display the contents of the specified commit, including the changes that were made.
