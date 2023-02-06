---
title: Bring in the upstream branch into the copy of the repository on github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can import an upstream branch into a fork by using the git fetch command.
---

**Contents**

[TOC]

# Section 1: Forking a Repository

Forking a repository is a process that allows users to create a copy of an existing repository on their own Github account. This gives users the ability to make changes to the code without altering the original repository.

# Section 2: Importing an Upstream Branch

An upstream branch is a branch in the original repository that has been forked. To import an upstream branch into a fork, users must first add the original repository as a remote to the forked repository. This can be done by running the command `git remote add upstream <url of original repository>`.

# Section 3: Merging the Upstream Branch

Once the original repository is added as a remote, users can merge the upstream branch into the forked repository by running the command `git merge upstream/<name of upstream branch>`. This will merge the changes from the original repository into the forked repository.

# Section 4: Pushing the Changes

Once the upstream branch has been merged, users can push the changes to the forked repository by running the command `git push origin <name of branch>`. This will push the changes to the forked repository, allowing users to have access to the changes from the original repository.
