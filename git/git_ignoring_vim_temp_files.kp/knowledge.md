---
title: Exclude vim temporary files from git tracking
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can add the line `*.swp` to the .gitignore file.
---

**Contents**

[TOC]

### Step 1: Create a .gitignore File

Create a `.gitignore` file in the root of your repository. This file should contain a list of all the files and folders that you want to ignore.

### Step 2: Add Vim Temporary Files to the .gitignore File

Add the following line to your `.gitignore` file:

```git
*.swp
```

This will ignore all files with the `.swp` extension, which are the temporary files created by Vim.

### Step 3: Commit the Changes

Once you have added the line to the `.gitignore` file, you need to commit the changes. This will ensure that the changes are applied to all future commits.

### Step 4: Push the Changes

Finally, push the changes to your remote repository. This will ensure that the changes are applied to all other users who have access to the repository.
