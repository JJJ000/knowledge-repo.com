---
title: How can I stop git from tracking a file that is now listed in .gitignore?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Run `git rm --cached <file>`, which will remove the file from version control but leave it in your working tree.
---

**Contents**

[TOC]

### Step 1: Remove the File from the Repository 

1. Check the status of the file: 
```shell
git status
```

2. Remove the file from the repository: 
```shell
git rm --cached <file>
```

### Step 2: Add the File to .gitignore 

1. Open the .gitignore file in a text editor.

2. Add the file to the .gitignore file. 

### Step 3: Commit Changes 

1. Commit the changes: 
```shell
git commit -m "Removed <file> from repository"
```

### Step 4: Push Changes 

1. Push the changes to the remote repository: 
```shell
git push origin <branch>
```
