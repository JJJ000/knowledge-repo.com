---
title: How should I proceed with a commit made in a detached head?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Checkout the commit to a branch to make it part of the project`s history.
---

**Contents**

[TOC]

#1 Re-Attach the Detached Head

The first step to dealing with a detached head is to re-attach it to a branch. This can be done using the `git checkout` command. For example, to re-attach the detached head to the master branch, you would use the following command:

```
git checkout master
```

#2 Merge the Detached Head

Once the detached head is re-attached to a branch, the next step is to merge the changes made in the detached head into the branch. This can be done with the `git merge` command. For example, if the detached head was made from the master branch, you could use the following command to merge the changes:

```
git merge detached-head
```

#3 Push the Changes

Once the changes from the detached head have been merged into the branch, the next step is to push the changes to the remote repository. This can be done with the `git push` command. For example, if the detached head was made from the master branch, you could use the following command to push the changes:

```
git push origin master
```

#4 Clean Up

Finally, once the changes have been pushed to the remote repository, it is important to clean up the local repository. This can be done with the `git branch -D` command. This will delete the detached head, ensuring that it will not be used again. For example, if the detached head was named `detached-head`, you could use the following command to delete it:

```
git branch -D detached-head
```
