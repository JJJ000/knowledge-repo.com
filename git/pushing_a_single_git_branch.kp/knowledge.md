---
title: What is the process for pushing only one git branch and not any others?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git push origin <branch\_name>` to push a single Git branch.
---

**Contents**

[TOC]

1. **Check Out the Branch:**  
    Use the `git checkout` command to switch to the desired branch:
    ```
    git checkout <branch-name>
    ```

2. **Push the Branch:**  
    Push the current branch to the remote repository with the `git push` command:
    ```
    git push origin <branch-name>
    ```

3. **Verify Push:**  
    Verify that the branch has been pushed successfully with the `git branch` command:
    ```
    git branch -r
    ```

4. **Clean Up:**  
    Switch back to the original branch with the `git checkout` command:
    ```
    git checkout <original-branch-name>
    ```
