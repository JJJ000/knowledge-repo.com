---
title: Do git forks function the same way as git clones?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Yes, Git forks are actually Git clones.
---

**Contents**

[TOC]

### Yes
Git forks are actually Git clones. A fork is a copy of a repository that allows you to freely experiment with changes without affecting the original project. When you fork a repository, you create a copy of the original repository in your own account on the hosting service. This copy is a Git clone, and it includes all of the original project’s files and history.

### No
A fork is not the same as a clone. A clone is a local copy of a repository that is entirely independent of the original repository. It does not have any of the original repository’s history, and changes to the clone do not affect the original repository in any way. A fork, on the other hand, is a copy of a repository that is linked to the original repository. Changes to the fork are reflected in the original repository, and vice versa.
