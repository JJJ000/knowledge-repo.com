---
title: Commit changes to .gitignore
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, changes to .gitignore will not take effect after commit.
---

**Contents**

[TOC]

### No

Git tracks changes to all files in a repository, regardless of whether they are included in the `.gitignore` file. After a file has been committed, it will remain in the repository even if it is later added to the `.gitignore` file.

### Yes

It is still possible to prevent files from being tracked after they have been committed. To do this, you must remove the file from the repository using the `git rm` command. This will delete the file from the repository, as well as any subsequent commits.
