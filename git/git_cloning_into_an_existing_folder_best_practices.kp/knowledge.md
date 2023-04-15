---
title: What is the recommended approach for cloning a repository into an existing directory using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The best practice to `git clone` into an existing folder is to use the `--depth` option to limit the amount of history that is downloaded.
---

**Contents**

[TOC]

### Step 1: Create a New Directory

The first step to cloning into an existing folder is to create a new directory. This new directory should be outside of the existing folder and should be named something distinct from the existing folder. For example, if the existing folder is named "my-project", the new directory could be named "my-project-clone".

### Step 2: Navigate to New Directory

Once the new directory has been created, open a terminal or command line and navigate to the new directory. This can be done by using the command `cd` followed by the name of the directory. For example, if the new directory is named "my-project-clone", the command would be `cd my-project-clone`.

### Step 3: Clone the Repository

Once the terminal or command line is navigated to the new directory, the repository can be cloned by using the command `git clone` followed by the URL of the repository. This will clone the repository into the new directory.

### Step 4: Move the Cloned Repository

The last step is to move the cloned repository into the existing folder. This can be done by using the command `mv` followed by the name of the cloned repository and the name of the existing folder. For example, if the repository is named "my-project-repo" and the existing folder is named "my-project", the command would be `mv my-project-repo my-project`.
