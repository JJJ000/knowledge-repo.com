---
title: What is the process for obtaining a single file from a different branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Checkout the file from the other branch using the `git checkout <branch> <file>` command.
---

**Contents**

[TOC]

### 1. Checkout the Desired Branch 

To get a single file from another branch, the first step is to checkout the desired branch. This can be done by using the `git checkout` command, followed by the name of the branch. 

```
git checkout <branch_name>
```

### 2. Copy the Desired File 

Once the desired branch is checked out, the desired file can be copied from the branch. This can be done by using the `cp` command, followed by the path of the file. 

```
cp <file_path> <destination_path>
```

### 3. Checkout the Original Branch 

After the desired file is copied, the original branch can be checked out. This can be done by using the `git checkout` command, followed by the name of the original branch. 

```
git checkout <branch_name>
```

### 4. Add and Commit the File 

Finally, the copied file can be added and committed to the original branch. This can be done by using the `git add` and `git commit` commands. 

```
git add <file_name>
git commit -m "<commit_message>"
```
