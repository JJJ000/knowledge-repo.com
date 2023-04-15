---
title: To convert an existing non-empty directory into a git working directory and push files to a remote repository, you will need to first initialize a git repository in the directory, add the files to the repository, commit the changes, and then push the repository to the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run the command `git init` in the existing directory, then `git add` and `git commit` the files, then `git remote add origin <repository URL>` and `git push -u origin master` to push the files to the remote repository.
---

**Contents**

[TOC]

1. Initialize a Git Repository

First, you need to initialize a Git repository in the directory you want to convert. To do this, open a terminal window in the directory and run the following command:

```
git init
```

2. Add Files to the Repository

Next, you need to add the existing files in the directory to the repository. To do this, run the following command:

```
git add .
```

3. Commit the Changes

Once the files have been added to the repository, you need to commit the changes. To do this, run the following command:

```
git commit -m "Initial commit"
```

4. Push the Changes to a Remote Repository

Finally, you need to push the changes to a remote repository. To do this, you need to add the remote repository URL to the local repository. To do this, run the following command:

```
git remote add origin <remote repository URL>
```

Once the remote repository has been added, you can push the changes to it with the following command:

```
git push -u origin master
```
