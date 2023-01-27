---
title: What is the process for changing the name of a git tag?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can rename a Git tag by using the `git tag -d <old\_name>` and `git tag <new\_name>` commands.
---

**Contents**

[TOC]

### Renaming a Git Tag

### Step 1: Delete the Old Tag

First, delete the old tag using the following command:

```
$ git tag -d <old_tag_name>
```

### Step 2: Create a New Tag

Create a new tag with the desired name using the following command:

```
$ git tag <new_tag_name>
```

### Step 3: Push the New Tag

Push the new tag to the remote repository using the following command:

```
$ git push origin <new_tag_name>
```

### Step 4: Verify the Tag

Verify that the tag was successfully renamed by running the following command:

```
$ git tag -l
```
