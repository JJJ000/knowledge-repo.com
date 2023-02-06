---
title: What are the advantages of using 'git rm' to delete a file instead of 'rm'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git rm allows for the removal of files to be tracked in the version control system, whereas rm only removes the file from the filesystem.
---

**Contents**

[TOC]

1. Version Control:
    Using `git rm` ensures that the file is removed from the repository, and that the changes are tracked in the repository's history. This allows developers to go back and view the changes that have been made to the repository over time.

2. Safety:
    Using `git rm` instead of `rm` ensures that the file is not accidentally deleted from the local filesystem. This is especially important when working with a remote repository, as it ensures that the changes made to the repository are consistent across all users.

3. Synchronization:
    Using `git rm` ensures that the file is removed from the repository and that all other users of the repository are aware of the change. This allows all users to stay up to date with the changes that have been made to the repository.

4. Reverting Changes:
    Using `git rm` allows developers to easily revert changes that have been made to the repository. This is especially useful when a file has been accidentally deleted, as it allows the file to be quickly restored to its original state.
