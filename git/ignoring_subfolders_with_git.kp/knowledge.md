---
title: What is the process for excluding subfolders/subdirectories from being tracked by git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To ignore subfolders/subdirectories, add the folder/directory name to the .gitignore file.
---

**Contents**

[TOC]

### Add a .gitignore File

1. Create a `.gitignore` file in the root directory of the repository.

2. Add the name of the subfolder/subdirectory you want to ignore to the `.gitignore` file.

### Commit the .gitignore File

1. Commit the `.gitignore` file to the repository.

2. Push the changes to the remote repository.

### Verify Ignored Subfolder/Subdirectory

1. Check the status of the repository to verify that the subfolder/subdirectory is being ignored.

2. Make changes to the subfolder/subdirectory and check the status again.

### Troubleshooting

1. If the subfolder/subdirectory is still being tracked, check the syntax of the `.gitignore` file.

2. If the syntax is correct, check the `.gitignore` file for any typos.

3. If the problem persists, contact a Git expert for help.
