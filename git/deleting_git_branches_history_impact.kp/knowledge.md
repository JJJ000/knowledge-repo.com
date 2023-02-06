---
title: Will deleting a branch in git remove all traces of it from the repository's history?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, deleting a branch in git does not remove it from the history.
---

**Contents**

[TOC]

## No
Deleting a branch in git does not remove it from the history. When a branch is deleted, it is not completely removed from the repository. The branch still exists in the repository's object database and can be recovered.

## Reasons
The main reason why deleting a branch does not remove it from the history is because git stores all changes to the repository in the form of commits. When a branch is deleted, the commits that were made on that branch are still stored in the repository and can be accessed through the git log command. 

## Recovering
It is possible to recover a deleted branch by using the git reflog command. This command will show all of the changes that have been made to the repository, including the deletion of a branch. From there, it is possible to use the git checkout command to restore the deleted branch. 

## Conclusion
In conclusion, deleting a branch in git does not remove it from the history. The commits that were made on the branch are still stored in the repository and can be recovered using the git reflog and git checkout commands.
