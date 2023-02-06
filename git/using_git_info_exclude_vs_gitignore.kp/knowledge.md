---
title: What is the purpose of using .git/info/exclude instead of .gitignore to exclude files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The .git/info/exclude file should be used if you want the exclusion rules to apply only to a single repository and not be shared with other clones.
---

**Contents**

[TOC]

**When To Use .git/info/exclude**
1. When Excluding Files From All Repositories
   If you want to exclude certain files from all of the repositories on your local machine, then you should use the .git/info/exclude file. This will ensure that the files are excluded from all repositories, regardless of whether they are in the same directory or not.

2. When Excluding Files From A Specific Repository
   If you want to exclude certain files from a specific repository, then you should use the .gitignore file in that repository. This will ensure that the files are excluded from that repository only, and not from any other repositories on your machine.

3. When Excluding Files From A Subdirectory
   If you want to exclude certain files from a specific subdirectory of a repository, then you should use the .git/info/exclude file. This will ensure that the files are excluded from the subdirectory only, and not from the repository as a whole.

4. When Excluding Files From A Remote Repository
   If you want to exclude certain files from a remote repository, then you should use the .git/info/exclude file. This will ensure that the files are excluded from the remote repository only, and not from any other repositories on your machine.
