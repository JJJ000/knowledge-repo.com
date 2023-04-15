---
title: Is there a version of "git merge -s ours" that is specifically for "theirs"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: No, there is not a `theirs` version of `git merge -s ours`.
---

**Contents**

[TOC]

#Yes

####What is 'git merge -s ours'?

Git merge -s ours is a type of merge strategy that is used when merging branches. It takes the changes from the current branch and discards all of the changes from the other branch. This is useful when you want to keep the changes from the current branch and discard the changes from the other branch.

####What is 'git merge -s theirs'?

Git merge -s theirs is the opposite of git merge -s ours. It takes the changes from the other branch and discards all of the changes from the current branch. This is useful when you want to keep the changes from the other branch and discard the changes from the current branch.

####How to Use 'git merge -s theirs'?

To use 'git merge -s theirs', you need to specify the strategy when running the 'git merge' command. For example, if you are merging branch 'A' into branch 'B', you would run the following command:

git merge -s theirs A B

This will take the changes from branch 'A' and discard all of the changes from branch 'B'.
