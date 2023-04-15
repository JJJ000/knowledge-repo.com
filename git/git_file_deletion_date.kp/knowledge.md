---
title: Determine when a file was removed from a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: It is not possible to determine when a file was deleted in Git.
---

**Contents**

[TOC]

#1 How to Check File History

Git stores a history of all changes made to a file, including when it was deleted. To check the file history, you can use the `git log` command. This command will show a list of all commits that have been made to the file, including when it was deleted.

#2 How to Find the Commit Where the File Was Deleted

If you want to find the commit where the file was deleted, you can use the `git log --diff-filter=D` command. This command will show a list of all commits that have deleted a file, including when it was deleted.

#3 How to Find the Date When the File Was Deleted

Once you have found the commit where the file was deleted, you can use the `git show` command to view the commit details. This will show the date when the file was deleted, as well as other information about the commit.

#4 How to View the File Contents Before It Was Deleted

If you want to view the contents of the file before it was deleted, you can use the `git show` command with the commit hash of the commit where the file was deleted. This will show the contents of the file before it was deleted.
