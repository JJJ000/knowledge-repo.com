---
title: Include a .gitignore file in the git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you should add a .gitignore file to your repository to specify which files should be ignored by Git.
---

**Contents**

[TOC]

# Section 1: What is .gitignore?

.gitignore is a file that tells Git which files or folders to ignore when committing changes to a repository. It is commonly used to prevent certain files from being added to a repository, such as configuration files, sensitive data, and compiled binaries.

# Section 2: Why Should You Add .gitignore?

Adding .gitignore to a repository is important for several reasons. It helps keep your repository clean by preventing unnecessary files from being added. It also prevents sensitive data from being accidentally committed to a public repository, which could be a security risk.

# Section 3: How to Add .gitignore

Adding .gitignore to a repository is simple. First, create a file called `.gitignore` in the root of your repository. Then, add the names of the files or folders you want to ignore to the `.gitignore` file. Finally, commit the changes to the repository.

# Section 4: Examples of Files to Add to .gitignore

Some common examples of files that should be added to .gitignore include: configuration files (e.g. `.env`), compiled binaries (e.g. `.exe`), and sensitive data (e.g. `.key`). Additionally, it is a good idea to add any file or folder that is not necessary for the project to function.
