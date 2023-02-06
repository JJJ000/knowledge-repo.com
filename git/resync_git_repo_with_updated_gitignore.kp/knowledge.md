---
title: Synchronize the git repository with the updated .gitignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git rm -r --cached .` followed by `git add .` to update the repo with the new .gitignore file.
---

**Contents**

[TOC]

1. Add .gitignore File to Repo

- Create a .gitignore file in the root directory of the repository
- Add the desired contents to the .gitignore file
- Add the .gitignore file to the repository with the following command:
```
git add .gitignore 
```

2. Commit the .gitignore File

- Commit the .gitignore file to the repository with the following command:
```
git commit -m "Added .gitignore file"
```

3. Push the Changes

- Push the changes to the remote repository with the following command:
```
git push origin master
```

4. Pull the Changes

- Pull the changes from the remote repository with the following command:
```
git pull origin master
```
