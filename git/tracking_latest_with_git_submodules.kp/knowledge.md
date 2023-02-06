---
title: Track the latest version of a git submodule
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git submodules track the specific commit of the submodule repository that is referenced in the parent repository.
---

**Contents**

[TOC]

# Section 1 - Initializing Submodules

To ensure that a submodule is tracking the latest version of the repository, the first step is to initialize the submodule. This can be done by navigating to the root directory of the repository and running the following command: 

```
git submodule init
```

# Section 2 - Updating Submodules

Once the submodule has been initialized, the next step is to update the submodule to the latest version of the repository. This can be done by running the following command:

```
git submodule update
```

# Section 3 - Tracking Submodule Changes

After the submodule has been updated, it is important to track any changes that may have been made to the repository. This can be done by running the following command:

```
git submodule foreach git pull origin master
```

# Section 4 - Committing Submodule Changes

Finally, any changes that have been made to the submodule should be committed to the repository. This can be done by running the following command:

```
git commit -am "Updated submodule to latest version"
```
