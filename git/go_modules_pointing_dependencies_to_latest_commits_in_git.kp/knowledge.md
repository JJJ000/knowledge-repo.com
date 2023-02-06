---
title: What is the best way to reference the most recent commit in a repository when setting up a go module dependency in go.mod?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In the go.mod file, specify the commit hash of the desired version as the version for the module dependency.
---

**Contents**

[TOC]

# Section 1: Cloning the Repo

The first step is to clone the desired repo. This can be done by running the following command in your terminal:

```
git clone <repo_url>
```

# Section 2: Checking Out the Latest Commit

Once the repo has been cloned, you can check out the latest commit by running the following command:

```
git checkout <commit_hash>
```

# Section 3: Updating go.mod

Once you have the latest commit checked out, you can update the go.mod file to point to the new commit. This can be done by running the following command:

```
go mod edit -replace <old_dependency>=<repo_url>@<commit_hash>
```

# Section 4: Installing Dependencies

Finally, you can install the dependencies by running the following command:

```
go get -u <repo_url>@<commit_hash>
```
