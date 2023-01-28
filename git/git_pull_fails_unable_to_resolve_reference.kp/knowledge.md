---
title: The 'git pull' command failed with the errors "unable to resolve reference" and "unable to update local ref"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: This is likely caused by a conflict between the local and remote versions of the repository, and can be resolved by resolving the conflict and then pulling again.
---

**Contents**

[TOC]

### Check Local Repository

The first step to troubleshoot this issue is to check the local repository. This can be done by running `git reflog` to identify any changes that have been made to the local repository. If any changes have been made, they should be reverted before attempting to pull from the remote repository.

### Check Remote Repository

The next step is to check the remote repository. This can be done by running `git ls-remote` to see if the reference is available on the remote repository. If the reference is not available on the remote repository, it will need to be added before attempting to pull from the remote repository.

### Update Local Ref

If the reference is available on the remote repository, the local ref needs to be updated. This can be done by running `git fetch` to fetch the reference from the remote repository and then running `git update-ref` to update the local ref.

### Pull From Remote Repository

Once the local ref has been updated, the next step is to pull from the remote repository. This can be done by running `git pull` to pull the changes from the remote repository. If the pull is successful, the reference should now be available in the local repository.
