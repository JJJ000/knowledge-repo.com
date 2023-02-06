---
title: Transferring git repository content to a different repository while maintaining its history
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Clone the repository and use the `git push` command to push the content to the new repository, preserving the history.
---

**Contents**

[TOC]

# Section 1: Clone the Repository

The first step in transferring content from one repository to another is to clone the repository you want to transfer content from. This can be done with the following command:

`git clone <repo_url>`

Where `<repo_url>` is the URL of the repository you want to clone.

# Section 2: Add the New Repository

Once the repository has been cloned, you need to add the new repository you want to transfer content to. This can be done with the following command:

`git remote add <new_repo_url>`

Where `<new_repo_url>` is the URL of the new repository you want to transfer content to.

# Section 3: Push the Content

Once the new repository has been added, you can push the content from the old repository to the new one with the following command:

`git push <new_repo_url> --all`

This will push all the content from the old repository to the new one, preserving the commit history.

# Section 4: Clean Up

Once the content has been successfully transferred, you can clean up the old repository by deleting it. This can be done with the following command:

`git remote rm <old_repo_url>`

Where `<old_repo_url>` is the URL of the old repository you want to delete.
