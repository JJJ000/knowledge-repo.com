---
title: There is a problem when attempting to add common code as a git submodule it is already present in the index
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The issue is that the submodule has already been added to the index.
---

**Contents**

[TOC]

### Introduction
Adding common code as a git submodule can be a useful way to share code between different projects. However, it can sometimes be difficult to add the code as a submodule if you encounter an error message saying "already exists in the index". This error can be caused by a variety of factors, and it can be difficult to know how to proceed. In this article, we will discuss the potential causes of this error and how to resolve it.

### Causes of the Error
The most common cause of this error is that the submodule is already present in the repository. This can happen if the submodule was added to the repository in the past, but was then removed. In this case, the submodule will still exist in the index, but will not be visible in the repository.

Another potential cause of this error is that the submodule is already present in another repository. This can happen if the same submodule is used in multiple repositories. In this case, the submodule will be present in the index of each repository, but will not be visible in any of them.

### Resolving the Error
The first step to resolving this error is to determine the cause. If the submodule is present in the repository, then it can be removed using the `git rm` command. If the submodule is present in another repository, then it should be removed from that repository first.

Once the cause has been determined, the submodule can be added again using the `git submodule add` command. This will add the submodule to the repository, and it should be visible in the repository after this command is run.

### Conclusion
Adding common code as a git submodule can be a useful way to share code between different projects. However, it can sometimes be difficult to add the code as a submodule if you encounter an error message saying "already exists in the index". This error can be caused by a variety of factors, and it can be difficult to know how to proceed. In this article, we have discussed the potential causes of this error and how to resolve it.
