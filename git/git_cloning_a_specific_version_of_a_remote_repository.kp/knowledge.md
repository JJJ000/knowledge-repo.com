---
title: Clone a specific version of a remote repository using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can clone a particular version of a remote repository by specifying a tag or commit hash when cloning.
---

**Contents**

[TOC]

1. Cloning the Remote Repository

To clone a particular version of the remote repository, you need to first clone it using the `git clone` command.

```
git clone https://github.com/username/repo.git
```

2. Checkout the Desired Version

Once you have cloned the repository, you can switch to the desired version using the `git checkout` command.

```
git checkout <tag_name>
```

3. Pull the Version

Once you have checked out the desired version, you can pull the version using the `git pull` command.

```
git pull origin <tag_name>
```

4. Push the Version

Finally, you can push the version to the remote repository using the `git push` command.

```
git push origin <tag_name>
```
