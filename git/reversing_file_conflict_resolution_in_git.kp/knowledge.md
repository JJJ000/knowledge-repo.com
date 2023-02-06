---
title: Revert a single file to a state before conflict resolution was applied
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To restart/undo conflict resolution in a single file in Git, use the `git checkout -- <file>` command.
---

**Contents**

[TOC]

# Step 1: Checkout the File

In order to undo conflict resolution in a single file in Git, the first step is to checkout the file. To do this, you will need to use the `git checkout` command. The syntax for this command is: 

```
git checkout <branch name> <file name>
``` 

This command will allow you to checkout the file from the specified branch. 

# Step 2: Reset the File

Once the file has been checked out, you will need to reset the file to its original state. To do this, you will need to use the `git reset` command. The syntax for this command is: 

```
git reset --hard <commit SHA> <file name>
```

This command will reset the file to the specified commit SHA. 

# Step 3: Add the File

The next step is to add the file back to the staging area. To do this, you will need to use the `git add` command. The syntax for this command is: 

```
git add <file name>
```

This command will add the file to the staging area. 

# Step 4: Commit the File

Finally, you will need to commit the file. To do this, you will need to use the `git commit` command. The syntax for this command is: 

```
git commit -m "Commit message" <file name>
```

This command will commit the file with the specified commit message.
