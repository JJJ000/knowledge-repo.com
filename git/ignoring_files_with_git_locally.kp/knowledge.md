---
title: What steps do I need to take to set up git to not track certain files on my computer?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Create a `.gitignore` file in the root directory of the repository and list the files/directories that should be ignored.
---

**Contents**

[TOC]

### Step 1: Create a .gitignore File

Create a file in the root of your Git repository called `.gitignore`. This file should contain a list of file patterns to ignore when pushing files to your repository.

### Step 2: Add File Patterns

Add the file patterns of the files and/or folders you want to ignore to the `.gitignore` file. For example, if you want to ignore all `.log` files in the root of your repository, you would add the following line to the `.gitignore` file:

```git
*.log
```

### Step 3: Commit the .gitignore File

Once you have added the file patterns to your `.gitignore` file, commit the file to your repository. This will ensure that the files you have specified in the `.gitignore` file will be ignored when pushing files to your repository.

### Step 4: Push Changes

Finally, push your changes to the remote repository. Your specified files will now be ignored when pushing files to the repository.
