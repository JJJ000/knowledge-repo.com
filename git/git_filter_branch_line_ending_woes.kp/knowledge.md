---
title: I am attempting to use git filter-branch to resolve line-ending issues but have not been successful
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Check out the other solutions on Stack Overflow, as the issue may be more complex than a simple filter-branch command.
---

**Contents**

[TOC]

### Solution 1: Using .gitattributes

1. Create a `.gitattributes` file in the root of your repository with the following content:

```git
* text=auto
```

2. Add the `.gitattributes` file to your repository with `git add .gitattributes`.

3. Commit the changes with `git commit -m "Add .gitattributes to fix line-endings"`.

### Solution 2: Using git filter-branch

1. Run the following command in the root of your repository:

```git
git filter-branch --tree-filter 'find . -type f -exec dos2unix {} \;' --prune-empty HEAD
```

2. Push the changes to the remote repository with `git push --force`.

3. Clean up the local repository with `git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch .gitattributes' --prune-empty --tag-name-filter cat -- --all`.
