---
title: Find the commit history for a particular line in a file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the git blame command to view the commit log for a specific line in a file in Git.
---

**Contents**

[TOC]

#1 Retrieve the SHA

The first step in retrieving the commit log for a specific line in a file in Git is to retrieve the SHA (Secure Hash Algorithm) of the commit that contains the line in question. This can be done by using the `git blame` command. This command will output the SHA of the commit that last modified the specified line.

#2 Retrieve the Commit Log

Once the SHA of the commit is known, the commit log can be retrieved by using the `git log` command. This command will output the commit log for the specified commit, including the commit message and the author of the commit.

#3 Retrieve the Diff

In addition to the commit log, it is also possible to retrieve the diff (or the difference) between the current version of the file and the version of the file at the time of the commit. This can be done by using the `git diff` command and specifying the SHA of the commit. This will output the diff between the two versions of the file.

#4 Retrieve the File

Finally, it is possible to retrieve the version of the file that was committed at the time of the commit by using the `git show` command and specifying the SHA of the commit. This will output the contents of the file at the time of the commit.
