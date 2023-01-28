---
title: "git remote add..." is a command used to add a remote repository to a local repository. "git push origin master" is a command used to push the local repository changes to the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: `git remote add ...` is used to add a remote repository to the local repository, and `git push origin master` is used to push the local repository`s master branch to the remote repository.
---

**Contents**

[TOC]

### git remote add

git remote add is a command used to add a remote repository. It takes two arguments: a remote name, for example `origin`, and a remote URL. The command creates a new remote named `origin` pointing at the URL you just specified.

### git push origin master

git push origin master is a command used to push the changes from your local repository to the remote repository. The command takes two arguments: the remote, which is `origin`, and the branch to be pushed, which is `master`. This command will push all commits from your local master branch to the remote repository's master branch.
