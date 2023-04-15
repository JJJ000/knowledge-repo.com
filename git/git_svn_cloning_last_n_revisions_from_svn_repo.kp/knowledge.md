---
title: What is the process for cloning the most recent n revisions from a subversion repository using git-svn?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `--revision` option with `git-svn clone` to clone the last n revisions from a Subversion repository.
---

**Contents**

[TOC]

### Install git-svn

In order to clone the last n revisions from a Subversion repository, you must first install git-svn. Git-svn is a tool that allows you to interact with a Subversion repository from a git repository.

### Clone the Repository

Once git-svn is installed, you can clone the Subversion repository using the following command:

```git
git svn clone --revision <n> <svn_url>
```

Where `<n>` is the number of revisions you want to clone, and `<svn_url>` is the URL of the Subversion repository.

### Checkout the Last n Revisions

Once the repository is cloned, you can check out the last n revisions using the following command:

```git
git checkout -b <branch_name> <revision_hash>
```

Where `<branch_name>` is the name of the branch you want to check out, and `<revision_hash>` is the hash of the revision you want to check out.

### Push to Remote

Once the last n revisions have been checked out, you can push the changes to a remote repository using the following command:

```git
git push --set-upstream <remote_name> <branch_name>
```

Where `<remote_name>` is the name of the remote repository, and `<branch_name>` is the name of the branch you want to push.
