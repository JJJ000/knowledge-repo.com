---
title: Exclude files from being included in a git merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use a .gitignore file to specify which files and directories should be ignored during a merge.
---

**Contents**

[TOC]

### Step 1: Create the .gitignore File

The first step to ignoring files during a merge is to create a `.gitignore` file. This file is used to specify which files and directories should be ignored by Git. It should be placed in the root directory of your repository.

### Step 2: Add File Patterns

Once the `.gitignore` file is created, you can add patterns for the files and directories you want to ignore. Each pattern should be listed on a separate line. For example, if you want to ignore all files with the `.pdf` extension, you would add the following line to the `.gitignore` file:

```
*.pdf
```

### Step 3: Commit the .gitignore File

Once you have added the patterns to the `.gitignore` file, you need to commit it to your repository. This will ensure that the changes are applied during the merge.

### Step 4: Perform the Merge

Finally, you can perform the merge as normal. Git will automatically ignore any files or directories that match the patterns in the `.gitignore` file.
