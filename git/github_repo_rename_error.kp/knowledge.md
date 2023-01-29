---
title: The repository has been relocated. please use the updated address
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You need to update the remote URL of your local repository to the new repository URL on GitHub.
---

**Contents**

[TOC]

### Solution

### Overview
When attempting to push a commit to a repository that has been renamed in GitHub, you may encounter the error message "remote: This repository moved. Please use the new location". This error occurs when the local repository is not updated with the new repository name. 

### Cause
When a repository is renamed in GitHub, the remote URL associated with the repository is changed. If the local repository is not updated with the new remote URL, the push operation will fail.

### Resolution
To resolve this error, you must update the local repository with the new remote URL. This can be done by running the following command in the terminal:

```git
git remote set-url origin [new_url]
```

Where `[new_url]` is the new remote URL associated with the repository.

### Conclusion
Once the local repository is updated with the new remote URL, the push operation should succeed.
