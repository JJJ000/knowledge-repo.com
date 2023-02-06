---
title: I cannot locate the new remote branch on git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git fetch` to download the new remote branch and make it visible locally.
---

**Contents**

[TOC]

## Understanding the Problem
Git is a version control system which helps developers store and manage changes to their code. When working in a team, it is common to use a remote repository to store code and collaborate on projects. When a new branch is created on the remote repository, it may not be visible to other team members.

## Possible Causes
There are several possible causes for this issue. The most common causes are:

1. The branch has not been pushed to the remote repository.
2. The repository has not been updated to reflect the new branch.
3. The branch has been deleted from the remote repository.

## Troubleshooting

1. Check if the branch has been pushed to the remote repository. To do this, run the command `git push --all` which will push all local branches to the remote repository.

2. Update the repository by running the command `git fetch --all`. This will download all the changes from the remote repository and make them available locally.

3. Check if the branch has been deleted from the remote repository. To do this, run the command `git branch -a` which will list all branches in the remote repository. If the branch is not listed, it has been deleted.

## Conclusion
If the branch is not visible after following the steps above, it is likely that the branch has been deleted from the remote repository. In this case, it is best to contact the repository owner and ask them to restore the branch.
