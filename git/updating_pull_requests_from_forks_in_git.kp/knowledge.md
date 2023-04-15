---
title: How can I make changes to a pull request on a repository I have forked?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Fetch the changes from the upstream repository, then merge them into your local forked repository and push the changes to your forked repository.
---

**Contents**

[TOC]

### Fetching the Changes from the Upstream Repository
1. Open a terminal window and navigate to the local repository of your forked repository.
2. Run the command `git remote -v` to view the list of configured remotes.
3. Run the command `git remote add upstream <upstream repository URL>` to add the upstream repository.
4. Run the command `git fetch upstream` to fetch the changes from the upstream repository.

### Merging the Changes from the Upstream Repository
1. Run the command `git checkout master` to switch to the local master branch.
2. Run the command `git merge upstream/master` to merge the changes from the upstream repository.

### Pushing the Merged Changes to the Forked Repository
1. Run the command `git push origin master` to push the merged changes to the forked repository.

### Updating the Pull Request
1. Navigate to the pull request page on the forked repository.
2. Click on the "Update pull request" button to update the pull request with the merged changes.
