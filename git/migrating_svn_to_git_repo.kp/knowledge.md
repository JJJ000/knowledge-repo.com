---
title: What is the process for transferring an svn repository with its timeline to a new git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the `git svn clone` command to migrate an SVN repository with history to a new Git repository.
---

**Contents**

[TOC]

1. **Prepare the SVN Repository**

- Ensure that the SVN repository is clean, with no uncommitted changes.
- Create a dump file of the SVN repository using `svnadmin dump`

2. **Create the Git Repository**

- Create a new, empty Git repository using `git init`
- Import the SVN dump file into the Git repository using `git svn clone`

3. **Configure the Git Repository**

- Configure the Git repository to use the same branches and tags as the SVN repository using `git config`
- Set the remote repository using `git remote add`

4. **Migrate the SVN Repository to Git**

- Pull the SVN repository into the Git repository using `git svn fetch`
- Push the Git repository to the remote repository using `git push -u origin master`
