---
title: What is the best way to prevent git from tracking future changes to a file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can add the file to your .gitignore file so that git will ignore all future revisions to the file.
---

**Contents**

[TOC]

1.  **Create a Global Git Ignore File**

- Create a `.gitignore` file in the root directory of your repository.
- Add the path of the file that you want to ignore to the `.gitignore` file.
- Commit the `.gitignore` file to your repository.

2. **Ignore a Single File**

- Create a `.git/info/exclude` file in the root directory of your repository.
- Add the path of the file that you want to ignore to the `.git/info/exclude` file.

3. **Ignore Multiple Files**

- Create a `.git/info/exclude` file in the root directory of your repository.
- Add a wildcard pattern to the `.git/info/exclude` file that matches the files that you want to ignore.

4. **Ignore a Folder**

- Create a `.gitignore` file in the root directory of your repository.
- Add the path of the folder that you want to ignore to the `.gitignore` file.
- Commit the `.gitignore` file to your repository.
