---
title: What commit does a tag reference in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The commit a tag points to can be determined by running the command `git rev-list -n 1 <tagname>`.
---

**Contents**

[TOC]

### Using `git tag`

1. Run the command `git tag` to list all tags in the repository.
2. Find the tag you are interested in and note its commit ID.
3. Run the command `git log <commit ID>` to view the commit the tag points to.

### Using `git show`

1. Run the command `git show <tag name>` to view the commit the tag points to.
2. Note the commit ID from the output of the command.
3. Run the command `git log <commit ID>` to view the commit the tag points to.
