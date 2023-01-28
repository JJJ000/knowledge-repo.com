---
title: The changes were not accepted because the most recent commit on your local branch is not in sync with the version on the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You must pull the remote branch changes before you can push your local branch changes.
---

**Contents**

[TOC]

### Problem Overview
When attempting to push changes to a remote repository in Git, you may encounter an error message indicating that your updates were rejected because the tip of your current branch is behind its remote counterpart. This error is caused by the fact that the remote repository has been updated with commits that are not present in your local repository.

### Causes of the Error
This error can be caused by a few different scenarios. One of the most common is when another developer has pushed changes to the remote repository while you were working on the same branch. In this case, the remote repository will contain commits that are not present in your local repository, causing the error when you attempt to push your changes.

Another common cause of this error is when a branch is rebased or merged with a different branch, resulting in the remote repository containing commits that are not present in your local repository.

### Solutions
The easiest way to resolve this error is to ensure that your local repository is up to date with the remote repository. This can be done by running the command `git pull` from the command line. This will pull any new commits from the remote repository and update your local repository with the latest changes.

If you are unable to pull the changes from the remote repository, you may need to manually merge the conflicting commits. This can be done by using the `git merge` command to manually merge the commits from the remote repository into your local repository.

Once the conflicts have been resolved, you should be able to push your changes to the remote repository without any further issues.
