---
title: What is the process for uploading files and folders to a github repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To add files and folders into a GitHub repository, use the `git add` command.
---

**Contents**

[TOC]

1. **Clone the Repository**

- Open up the command line and navigate to the directory where you would like to store the repository.
- Run the command `git clone <repository-url>` to clone the repository to your local machine. 

2. **Create or Add Files**

- Create or add the files you would like to upload to the repository.
- Add the files to the staging area by running the command `git add <filename>`.

3. **Commit the Changes**

- Commit the changes to the repository by running the command `git commit -m "<commit message>"`.

4. **Push the Changes**

- Push the changes to the repository by running the command `git push origin <branch-name>`.
