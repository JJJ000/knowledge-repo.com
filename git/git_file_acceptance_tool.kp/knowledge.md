---
title: A straightforward way to apply either 'accept theirs' or 'accept mine' to an entire file with git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The `git checkout --ours/--theirs` command can be used to accept either one`s changes on a whole file.
---

**Contents**

[TOC]

### Git Command

The following command can be used to accept theirs or accept mine on a whole file using git:

`git checkout --theirs <file>`

This command will accept the version of the file from the remote repository, overriding any local changes.

### Git GUI

If a GUI is preferred, most graphical Git clients have a feature to accept theirs or accept mine.

In the case of GitHub Desktop, this can be done by opening the file in conflict, selecting the version you wish to keep, and then clicking the “Accept Merge” button.

### Merge Conflicts

It’s important to note that if there are multiple conflicts in the file, this command or feature will only resolve the first conflict. The other conflicts will need to be manually resolved.

### Summary

In summary, to accept theirs or accept mine on a whole file using git, you can use the command `git checkout --theirs <file>` or use the feature in a graphical Git client. However, if there are multiple conflicts in the file, they will need to be manually resolved.
