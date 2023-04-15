---
title: What is the purpose of a git tag? how do you create tags? how do you check out a tag from a remote git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git tag is a lightweight reference to a specific commit, which can be created with the `git tag` command and checked out with the `git checkout` command.
---

**Contents**

[TOC]

### What is git tag

Git tag is a lightweight reference to a specific commit in a repository. It is commonly used to mark a specific version of a project, for example, a release version.

### How to create tags

To create a tag, you can use the git tag command. You can specify the tag name, the commit to which the tag should refer to, and an optional message.

For example, to create a tag called "v1.0" for the latest commit, you can use the following command:

```git
git tag -a v1.0 -m "Release version 1.0"
```

### How to checkout git remote tag(s)

To checkout a tag from a remote repository, you can use the git checkout command. For example, to checkout the "v1.0" tag from a remote repository, you can use the following command:

```git
git checkout -b v1.0 origin/v1.0
```

This will create a local branch called "v1.0" that is tracking the remote tag. You can then use the branch as you would any other branch.
