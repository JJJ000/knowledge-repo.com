---
title: Examine the git log for the directory
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git log` command to view the git history for a folder.
---

**Contents**

[TOC]

# Using git log

Git log allows you to view the commit history for a particular folder. To view the commit history for a folder, you can use the following command:

`git log -- <folder_name>`

This will show the commits for the entire folder, including all its subdirectories.

# Using gitk

Gitk is a graphical tool for viewing the commit history of a repository. To view the commit history for a particular folder, you can use the following command:

`gitk -- <folder_name>`

This will open up a graphical view of the commits for the entire folder, including all its subdirectories.

# Using git show

Git show allows you to view the contents of a particular commit. To view the contents of a commit for a particular folder, you can use the following command:

`git show <commit_hash> -- <folder_name>`

This will show the contents of the commit for the entire folder, including all its subdirectories.

# Using git diff

Git diff allows you to compare the differences between two commits. To view the differences between two commits for a particular folder, you can use the following command:

`git diff <commit_hash_1> <commit_hash_2> -- <folder_name>`

This will show the differences between the two commits for the entire folder, including all its subdirectories.
