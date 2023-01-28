---
title: Ignoring files in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use a .gitignore file to specify which files and directories to ignore.
---

**Contents**

[TOC]

1. **Using .gitignore File**

- Create a .gitignore file in the root of your repository.
- Add a line for each file or folder you want to ignore.
- For example, if you want to ignore a file called “config.js”, add this line to your .gitignore file: `config.js`.
- To ignore an entire folder, add the folder name with a trailing slash. For example, if you want to ignore a folder called “build”, add this line to your .gitignore file: `build/`.
- Commit the changes to the .gitignore file and push them to the remote repository.

2. **Using gitignore.io**

- Visit [gitignore.io](https://www.gitignore.io/) and enter the name of the language, framework, or editor for which you want to generate a .gitignore file.
- Copy the generated .gitignore file and paste it into the root of your repository.
- Commit the changes to the .gitignore file and push them to the remote repository.

3. **Using Git Commands**

- Use the `git rm --cached` command to ignore files that have already been added to the repository.
- For example, if you want to ignore a file called “config.js”, run this command: `git rm --cached config.js`.
- To ignore an entire folder, add the folder name with a trailing slash. For example, if you want to ignore a folder called “build”, run this command: `git rm --cached build/`.
- Commit the changes and push them to the remote repository.

4. **Using a Global .gitignore File**

- Create a global .gitignore file in your home directory.
- Add a line for each file or folder you want to ignore.
- For example, if you want to ignore a file called “config.js”, add this line to your global .gitignore file: `config.js`.
- To ignore an entire folder, add the folder name with a trailing slash. For example, if you want to ignore a folder called “build”, add this line to your global .gitignore file: `build/`.
- Run the `git config --global core.excludesfile` command to tell Git to use your global .gitignore file.
- Commit the changes and push them to the remote repository.
