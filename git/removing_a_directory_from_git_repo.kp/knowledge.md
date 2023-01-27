---
title: How can I delete a folder from a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the `git rm -r <directory>` command.
---

**Contents**

[TOC]

### 1. Locally

To remove a directory from a Git repository locally, use the following command:

```
git rm -r <directory-name>
```

This command will delete the directory from the local repository and stage the deletion for commit.

### 2. Remotely

To remove a directory from a Git repository remotely, use the following command:

```
git push origin --delete <directory-name>
```

This command will delete the directory from the remote repository.

### 3. Commit

Once the directory has been deleted locally and remotely, commit the changes by running the following command:

```
git commit -m "Removed <directory-name>"
```

### 4. Push

Finally, push the changes to the remote repository by running the following command:

```
git push origin master
```
