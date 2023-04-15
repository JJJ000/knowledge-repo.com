---
title: What is the total number of lines of code changed by a particular author in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git log --author <author> --numstat | awk `{ add += $1 ; subs += $2 } END { print `added lines ` add `, removed lines ` subs }`` to count total lines changed by a specific author in a Git repository.
---

**Contents**

[TOC]

### Install Git

In order to count the total lines changed by a specific author in a Git repository, you must first install Git. Git is a version control system that allows you to track changes made to a project over time.

### Clone the Repository

Once you have installed Git, you will need to clone the repository. Cloning the repository will create a local copy of the repository on your computer. You can do this by running the following command:

`git clone <repository-url>`

### Checkout Author

Once you have cloned the repository, you can check out the author you want to count the total lines changed by. This can be done by running the command:

`git checkout <author-name>`

### Count Lines Changed

Once you have checked out the author, you can then count the total lines changed by running the following command:

`git log --author="<author-name>" --oneline | wc -l`

This will output the total number of lines changed by the specified author.
