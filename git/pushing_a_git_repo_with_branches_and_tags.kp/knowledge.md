---
title: Upload the local git repository to a new remote server, including all branches and tags
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To push a local Git repo to a new remote, including all branches and tags, use the command `git push --all <remote\_name>`.
---

**Contents**

[TOC]

1. Create a New Remote Repository
------------------------
Create a new remote repository on your Git hosting service. Make sure to add a `.gitignore` and `LICENSE` file to the repo.

2. Push Existing Local Repository
------------------------
Once the remote repository has been created, run the following commands to push your existing local repository and its branches and tags to the remote repository:

```
git remote add origin <remote repository URL>
git push --all origin
git push --tags origin
```

3. Verify the Push
------------------------
Verify that your local repository was successfully pushed to the remote repository by running the following command:

```
git remote -v
```

4. Pull from the Remote
------------------------
Finally, pull from the remote repository to make sure all branches and tags were successfully pushed:

```
git pull origin --all
```
