---
title: What is the process for clearing all commit history in github?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: It is not possible to delete all commit history in GitHub.
---

**Contents**

[TOC]

### Deleting the Repository

The most comprehensive way to delete all commit history in GitHub is to delete the repository itself. This will remove all of the files and the commit history associated with the project.

### Deleting Branches

If you do not want to delete the entire repository, you can delete individual branches in order to remove the associated commit history. This can be done by navigating to the repository in GitHub, clicking on the "Branch" tab, and then selecting the branch you want to delete.

### Using the BFG Repo-Cleaner

The BFG Repo-Cleaner is a command-line tool that can be used to delete all commit history in a GitHub repository. It can be used to delete specific commits, or to delete all commits in a repository.

### Using Git Commands

Git commands can also be used to delete all commit history in a GitHub repository. This can be done by using the git rebase command to rewrite the commit history, or by using the git filter-branch command to filter out specific commits.
