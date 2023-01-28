---
title: Take the file out of the repository but keep a copy on your local device
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To remove a file from the repository while keeping it locally, use the command `git rm --cached <file>`.
---

**Contents**

[TOC]

1. Removing a File From the Repository
------------------------------------

- Open the command line.
- Change the current working directory to the local repository.
- Use the `git rm` command to remove the file from the repository.

```
$ git rm <file>
```

2. Committing the Changes
------------------------

- Commit the changes to the repository.

```
$ git commit -m “<message>”
```

3. Keeping the File Locally
---------------------------

- Use the `git update-index` command to keep the file locally.

```
$ git update-index --assume-unchanged <file>
```

4. Verifying the Changes
------------------------

- Verify the changes with the `git status` command.

```
$ git status
```
