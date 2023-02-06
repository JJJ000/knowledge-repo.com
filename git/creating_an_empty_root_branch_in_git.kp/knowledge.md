---
title: What is the process for creating an empty "root" branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the command `git checkout --orphan <branch-name>` to create a new, empty `root` branch in Git.
---

**Contents**

[TOC]

# Section 1: Create a New Branch

To create a new branch in Git, you can use the `git branch` command. This command will create a new branch with the name you provide. For example, to create a new branch called "root", you would run the following command:

```
git branch root
```

# Section 2: Check Out the New Branch

Once you have created the new branch, you will need to check it out in order to start making changes. To do this, you can use the `git checkout` command. For example, to check out the newly created "root" branch, you would run the following command:

```
git checkout root
```

# Section 3: Create an Empty Commit

Once you have checked out the new branch, you can create an empty commit in order to make sure that the branch is properly initialized. To do this, you can use the `git commit` command with the `--allow-empty` flag. For example, to create an empty commit on the "root" branch, you would run the following command:

```
git commit --allow-empty -m "Initialize root branch"
```

# Section 4: Push the Branch to the Remote

Finally, you will need to push the new branch to the remote in order to make it available to other users. To do this, you can use the `git push` command. For example, to push the "root" branch to the remote, you would run the following command:

```
git push origin root
```
