---
title: What is the procedure for accessing an earlier version of a file using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can view an old version of a file with Git by using the `git checkout` command.
---

**Contents**

[TOC]

### Step 1: Checkout the Desired Commit

Run the `git checkout` command followed by the commit hash to which you want to go back.

```
git checkout <commit-hash>
```

### Step 2: View the File

Run the `git show` command followed by the file name to view the file.

```
git show <file-name>
```

### Step 3: Return to Latest Commit

Run the `git checkout` command followed by the `master` branch to return to the latest commit.

```
git checkout master
```

### Step 4: View the File

Run the `git show` command followed by the file name to view the file.

```
git show <file-name>
```
