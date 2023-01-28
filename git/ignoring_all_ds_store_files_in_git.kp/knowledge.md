---
title: Exclude all .ds_store files from all directories and their subdirectories in the .gitignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, adding `.DS\_Store` to the .gitignore file will ignore all .DS\_Store files in every folder and subfolder.
---

**Contents**

[TOC]

`**` Find the Files**

1. Open the Terminal app.
2. Navigate to the root of the folder where the .DS_Store files are located.
3. Use the command `find . -name .DS_Store -print` to locate all of the .DS_Store files.

`**` Add the Files to the .gitignore File**

1. Create a file in the root folder called `.gitignore`.
2. Add the line `.DS_Store` to the `.gitignore` file.

`**` Commit the Changes**

1. Use the command `git add .gitignore` to add the `.gitignore` file to the repository.
2. Use the command `git commit -m "Added .gitignore file"` to commit the changes.

`**` Push the Changes**

1. Use the command `git push origin master` to push the changes to the remote repository.
