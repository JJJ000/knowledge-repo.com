---
title: Merging multiple git repositories
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The best way to combine multiple git repositories is to use the git subtree merge command.
---

**Contents**

[TOC]

## Section 1: Cloning the Repositories

The first step in combining multiple git repositories is to clone all of the repositories into the same directory. This can be done using the `git clone` command, which takes the URL of the repository as an argument. For example, if you wanted to clone the repository `https://github.com/user/repo1`, you would use the command `git clone https://github.com/user/repo1`.

## Section 2: Combining the Repositories

Once the repositories have been cloned, they can be combined by using the `git subtree` command. This command takes two arguments: the source repository and the destination repository. For example, if you wanted to combine `repo1` and `repo2`, you would use the command `git subtree add --prefix=repo1 repo2 master`. This command will add the contents of `repo2` into the directory `repo1` in the destination repository.

## Section 3: Merging the Repositories

Once the repositories have been combined, they can be merged using the `git merge` command. This command takes two arguments: the source repository and the destination repository. For example, if you wanted to merge `repo1` and `repo2`, you would use the command `git merge repo1 repo2`. This command will merge the contents of `repo1` and `repo2` into the destination repository.

## Section 4: Pushing the Changes

Once the repositories have been merged, the changes can be pushed to the remote repository using the `git push` command. This command takes the remote repository URL as an argument. For example, if you wanted to push the changes to the repository `https://github.com/user/repo1`, you would use the command `git push https://github.com/user/repo1`. This will push the changes to the remote repository, making them available to everyone.
