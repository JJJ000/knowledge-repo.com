---
title: What is the process for checking out a single file from a git repository without downloading the entire repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git checkout <branch> -- <file>` to sparsely checkout a single file from a git repository.
---

**Contents**

[TOC]

### Cloning the Repository

The first step to sparsely checkout a single file from a Git repository is to clone the repository. This can be done by running the following command:

```
git clone <repository-url>
```

### Sparse Checkout Configuration

Once the repository is cloned, the next step is to configure the sparse checkout option. This can be done by running the following command:

```
git config core.sparsecheckout true
```

### Adding the File to the Checkout List

The next step is to add the file that needs to be sparsely checked out to the checkout list. This can be done by running the following command:

```
echo <file-name> >> .git/info/sparse-checkout
```

### Pulling the File

Finally, the file can be pulled from the repository by running the following command:

```
git pull origin master
```
