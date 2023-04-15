---
title: Find out when a stash was made
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The creation date of a stash in Git can be obtained using the `git stash show -p` command.
---

**Contents**

[TOC]

1. What is Git Stash?
----------------
Git Stash is a feature of the version control system Git that allows users to save changes they have made to their local repository temporarily and then apply them later. It is also used to switch between branches.

2. How to Get the Creation Date of a Stash
----------------
The creation date of a stash can be retrieved by running the command `git stash show -p stash@{<stash_number>}`. This command will show the patch of the stash and the date of the patch will be the creation date of the stash.

3. Example
----------------
For example, to get the creation date of the stash with the number `3`, run the command `git stash show -p stash@{3}`. This will show the patch of the stash and the date of the patch will be the creation date of the stash.

4. Conclusion
----------------
In conclusion, the creation date of a stash in Git can be retrieved by running the command `git stash show -p stash@{<stash_number>}`. This command will show the patch of the stash and the date of the patch will be the creation date of the stash.
