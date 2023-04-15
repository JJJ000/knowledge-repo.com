---
title: No submodule was found in the .gitmodule file for the specified path, which is not a submodule
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No action is required since there is no submodule mapping.
---

**Contents**

[TOC]

### What is a Submodule Mapping?
A submodule mapping is a mapping of a path in a repository to a submodule. This mapping is typically stored in a file called `.gitmodule` which is located at the root of the repository. This mapping allows the repository to track changes to the submodule and its contents.

### What Happens When No Submodule Mapping is Found?
When no submodule mapping is found in the `.gitmodule` file, the repository will not be able to track changes to the path in question. This means that any changes made to the path will not be recorded in the repository.

### How Can I Add a Submodule Mapping?
If you want to add a submodule mapping for a path that is not currently a submodule, you can add it to the `.gitmodule` file. This can be done by adding the following lines to the `.gitmodule` file:

```git
[submodule "<path>"]
	path = <path>
	url = <url>
```

### What Else Should I Know?
When adding a submodule mapping, it is important to make sure that the path and URL are valid. Additionally, it is also important to make sure that the submodule is initialized and updated in order for the repository to track changes to the submodule.
