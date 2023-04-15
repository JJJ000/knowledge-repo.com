---
title: How can I incorporate unmerged pull requests from other forks into my own fork?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the `git cherry-pick` command to apply unmerged upstream pull requests from other forks into your fork.
---

**Contents**

[TOC]

### Find the Pull Request

The first step to applying an unmerged upstream pull request from another fork into your own fork is to find the pull request. If you know the exact pull request number, you can search for it directly in the upstream repository. If you don't know the exact number, you can search through the open pull requests to find the one you want.

### Fetch the Pull Request

Once you have located the pull request, you can fetch it in your own fork. To do this, you need to add the upstream repository to your local clone of your fork. You can do this by running the command `git remote add upstream <url-of-upstream-repo>`. Once you have added the upstream repository, you can fetch the pull request by running the command `git fetch upstream pull/<pull-request-number>/head:<name-of-branch>`.

### Merge the Pull Request

Once you have fetched the pull request, you can merge it into your own fork. To do this, you need to checkout the branch you want to merge the pull request into and then run the command `git merge <name-of-branch>`. This will merge the pull request into your own fork.

### Push the Changes

Once you have merged the pull request, you need to push the changes to your own fork. To do this, simply run the command `git push origin <name-of-branch>`. This will push the changes to your own fork, allowing you to access the changes in the pull request.
