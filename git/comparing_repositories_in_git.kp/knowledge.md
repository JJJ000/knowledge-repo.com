---
title: Determining the distinctions between two repositories
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The difference between two repositories in Git can be seen by running the command `git diff <repo1> <repo2>`.
---

**Contents**

[TOC]

### Cloning the Repositories

The first step in getting the difference between two repositories in Git is to clone the repositories. This can be done by running the command `git clone <url>` with the URL of the repository you are cloning.

### Comparing the Repositories

Once the repositories have been cloned, the next step is to compare the two repositories. This can be done by running the command `git diff <repo1> <repo2>` with the two repository names as the parameters. This will show the differences between the two repositories.

### Storing the Differences

If the differences between the two repositories need to be stored, they can be stored in a patch file. This can be done by running the command `git diff <repo1> <repo2> > <filename>.patch`. This will create a patch file with the differences between the two repositories.

### Applying the Patch

If the patch file needs to be applied to one of the repositories, it can be done by running the command `git apply <filename>.patch`. This will apply the patch file to the repository and make the changes to the code.
