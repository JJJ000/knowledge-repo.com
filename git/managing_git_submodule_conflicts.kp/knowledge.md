---
title: What is the best way to resolve conflicts when using git submodules?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Resolve conflicts in the submodule repository, then commit and push the change to the parent repository.
---

**Contents**

[TOC]

#### 1. Resolve Conflicts

When conflicts occur in a git submodule, it is important to resolve them as soon as possible. The first step is to identify the conflicting files:

`git submodule status`

Once the conflicting files have been identified, they can be resolved using the standard git conflict resolution process. This involves:

- Pulling the latest changes from the submodule's remote repository.
- Resolving any conflicts in the conflicting files.
- Committing the changes.
- Pushing the changes back to the remote repository.

#### 2. Update Submodule Reference

Once the conflicts have been resolved, the submodule reference must be updated to point to the new commit. This can be done using the following command:

`git submodule update --remote`

This will update the submodule reference to point to the latest commit in the remote repository.

#### 3. Commit Submodule Reference

Finally, the updated submodule reference must be committed to the main repository. This can be done with the following command:

`git commit -m "Updated submodule reference"`

This will commit the updated submodule reference to the main repository.

#### 4. Push Changes

Once the updated submodule reference has been committed, the changes must be pushed to the remote repository. This can be done with the following command:

`git push`

This will push the changes to the remote repository, ensuring that all users have access to the updated submodule reference.
