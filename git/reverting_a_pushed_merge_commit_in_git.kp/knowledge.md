---
title: What is the best way to undo a merge commit that has already been pushed to the remote repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git revert <merge\_commit\_SHA>` to create a new commit that reverts the changes of the merge commit.
---

**Contents**

[TOC]

### Revert Merge Commit Locally
1. Check out the branch that the merge commit was made to:  
`git checkout <branch-name>`
2. Create a new branch to store the reverted commit:  
`git branch <new-branch-name>`
3. Revert the merge commit:  
`git revert -m 1 <merge-commit-hash>`
4. Push the new branch to the remote repository:  
`git push origin <new-branch-name>`

### Merge Reverted Branch Back into Master
1. Check out the master branch:  
`git checkout master`
2. Merge the reverted branch into the master branch:  
`git merge <new-branch-name>`
3. Push the master branch to the remote repository:  
`git push origin master`

### Delete Reverted Branch
1. Check out the master branch:  
`git checkout master`
2. Delete the reverted branch:  
`git branch -d <new-branch-name>`
3. Push the master branch to the remote repository:  
`git push origin --delete <new-branch-name>`

### Clean Up Local Repository
1. Fetch the latest version of the remote repository:  
`git fetch origin`
2. Prune the local repository to remove any deleted branches:  
`git remote prune origin`
