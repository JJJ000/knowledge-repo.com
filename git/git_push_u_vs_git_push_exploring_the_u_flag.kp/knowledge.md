---
title: What is the difference between "git push -u origin master" and "git push origin master"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The `u` in `git push -u origin master` sets the upstream branch to the origin master branch, allowing for easier pushing and pulling of commits in the future.
---

**Contents**

[TOC]

**What is the “u” Flag?**

The “u” flag is an argument that can be passed to the “git push” command. It stands for “upstream” and is used to set the current branch’s upstream branch.

**What Does the “u” Flag Do?**

When the “u” flag is used, it tells Git to set the current branch’s upstream branch to the branch specified as the argument. This allows Git to track the current branch’s history, and makes it easier to push and pull changes between the local and remote branches.

**What is the Difference Between “git push -u origin master” and “git push origin master”?**

The difference between “git push -u origin master” and “git push origin master” is that the former sets the upstream branch of the local branch to the remote branch specified as the argument, while the latter simply pushes the local branch to the remote branch without setting the upstream branch.
