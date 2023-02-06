---
title: What is the process for removing the most recent n commits from both github and my local repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To delete the last n commits on Github and locally, use the `git reset --hard HEAD~n` command.
---

**Contents**

[TOC]

### Deleting Locally
1. Run `git log` to view the list of commits.
2. Copy the commit ID of the commit you want to revert back to.
3. Run `git reset --hard <commit_id>` to delete the last n commits.

### Deleting on Github
1. Run `git push -f origin <branch_name>` to force push the changes to Github.
2. Confirm the force push.
3. Go to the repository on Github and click on the "Commits" tab.
4. Click on the "Compare & pull request" tab.
5. Select the commits you want to delete and click on the "Delete commits" button.
6. Confirm the deletion.
