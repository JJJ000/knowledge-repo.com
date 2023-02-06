---
title: Files appearing as changed immediately after a git clone
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: This could be due to line endings being different between the local machine and the remote repository.
---

**Contents**

[TOC]

1. Cloning a Repository
When you clone a repository, you are downloading a copy of the project from a remote source. This includes all of the project's files, as well as the project's history.

2. Showing as Modified
When you clone a repository, all of the files will show up as modified. This is because the files are being tracked and stored locally, and the local version of the files are different from the remote version.

3. Git Status
If you run the command `git status`, you will see a list of all of the modified files. This is normal and expected after a clone.

4. Resolving the Changes
In order to resolve the changes, you need to commit the files. This will add the changes to the repository and update the local version of the files to match the remote version.
