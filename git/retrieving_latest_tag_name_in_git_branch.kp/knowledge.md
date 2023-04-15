---
title: What is the most recent tag name in my current git branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git describe --tags --abbrev=0` to get the latest tag name in the current branch.
---

**Contents**

[TOC]

1. Checkout the branch

In order to find the latest tag name in the current branch, you first need to checkout the branch. This can be done using the following command:

`git checkout <branch-name>`

2. List the Tags

Once you have checked out the branch, you can list all the tags associated with the branch using the following command:

`git tag -l`

3. Find the Latest Tag

The list of tags returned by the above command will be in the reverse chronological order. Hence, the first tag in the list will be the latest tag for the current branch.

4. Checkout the Latest Tag

Once you have identified the latest tag, you can checkout the tag using the following command:

`git checkout <tag-name>`
