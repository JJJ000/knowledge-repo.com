---
title: What is the process for working with a git repository that is nested within another repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use a Git submodule to work with a git repository within another repository.
---

**Contents**

[TOC]

### Cloning a Repository

Cloning a repository allows you to copy the repository and all of its contents to your local machine. This can be done with the `git clone` command. For example, if you wanted to clone a repository called `my-repo`, you would run the following command:

```
git clone https://github.com/username/my-repo.git
```

### Adding a Submodule

Once you have cloned the repository, you can add a submodule by running the `git submodule add` command. This will add the submodule to your repository and allow you to work with it. For example, if you wanted to add a submodule called `my-submodule` to your repository, you would run the following command:

```
git submodule add https://github.com/username/my-submodule.git
```

### Updating a Submodule

Once you have added a submodule, you can update it by running the `git submodule update` command. This will ensure that your local copy of the submodule is up to date with the remote repository. For example, if you wanted to update a submodule called `my-submodule`, you would run the following command:

```
git submodule update --remote my-submodule
```

### Removing a Submodule

If you no longer need a submodule, you can remove it by running the `git submodule deinit` command. This will remove the submodule from your repository. For example, if you wanted to remove a submodule called `my-submodule`, you would run the following command:

```
git submodule deinit my-submodule
```
