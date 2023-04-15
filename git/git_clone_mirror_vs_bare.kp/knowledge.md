---
title: What is the distinction between cloning a repository with the '--mirror' option and cloning a repository with the '--bare' option?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git clone --mirror creates a copy of the remote repository including all its branches and tags, while git clone --bare creates only the repository without any branches or tags.
---

**Contents**

[TOC]

### Git Clone --Mirror
Git clone --mirror creates a full mirror of a repository, including all branches and all tags. It also includes the remote tracking branches for each branch. This is useful for creating a backup of a repository, or for creating a repository that can be used as a remote repository for other repositories.

### Git Clone --Bare
Git clone --bare creates a repository without any of the working files or folders. It only includes the version control data, such as the commits, branches, and tags. This is useful for creating a remote repository that can be used by other repositories. It does not include any of the remote tracking branches.
