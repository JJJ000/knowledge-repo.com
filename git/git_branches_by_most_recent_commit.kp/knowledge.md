---
title: What is the best way to obtain a list of git branches, sorted by most recent commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the command `git for-each-ref --sort=-committerdate refs/heads/ --format=`%(refnameshort)`` to get a list of Git branches ordered by most recent commit.
---

**Contents**

[TOC]

### Install Git

In order to get a list of Git branches, you must first install Git. To do this, follow the instructions for your operating system found on the [Git website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

### Clone the Repository

Once Git is installed, you can clone the repository of interest. This can be done using the command `git clone <url>`.

### List the Branches

Once the repository is cloned, you can list the branches using the command `git branch -r --sort=-committerdate`. This will list all of the branches in the repository, sorted by the most recent commit date.

### Checkout the Branch

If you want to checkout a particular branch, you can use the command `git checkout <branch>`. This will switch you to the specified branch.
