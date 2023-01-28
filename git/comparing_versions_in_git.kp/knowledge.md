---
title: Comparing the current version to the previous version
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: The difference between the current and last version in Git can be found by using the `git diff` command.
---

**Contents**

[TOC]

### Identifying the Difference

Git can be used to identify the difference between the current version and the last version of a file. To do this, you would use the `git diff` command. This command can be used to compare two versions of a file, or to compare a file with the version in the staging area.

### Comparing Versions

When using the `git diff` command, you can specify the two versions of a file that you would like to compare. For example, to compare the current version of a file to the last version, you would use the command `git diff HEAD~1 HEAD`. This command will compare the current version of the file (HEAD) to the version that was committed one version back (HEAD~1).

### Viewing Changes

Once the two versions have been compared, Git will display the differences between them. This will show you the changes that were made in the current version of the file compared to the last version.

### Saving Changes

Once you have identified the differences between the two versions, you can use the `git commit` command to save the changes. This will commit the current version of the file to the repository, making it the most recent version.
