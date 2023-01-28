---
title: What is the command to commit all deleted files in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git commit -a` to commit all deleted files in Git.
---

**Contents**

[TOC]

### Delete Files

In order to commit all deleted files in Git, you must first delete the files from your local repository. This can be done by using the `git rm` command, followed by the file name:

```git
git rm <file_name>
```

### Commit Changes

Once the files have been deleted, you must commit the changes to your local repository. This can be done by using the `git commit` command:

```git
git commit -m "Committing all deleted files"
```

### Push to Remote Repository

Finally, in order to push the changes to the remote repository, you must use the `git push` command:

```git
git push origin master
```

### Verify Changes

Once the changes have been pushed, you can verify that the files have been deleted from the remote repository by running the `git status` command:

```git
git status
```

This will show the status of the repository, including any deleted files.
