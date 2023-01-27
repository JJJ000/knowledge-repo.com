---
title: Retrieve a particular tag using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To download a specific tag with Git, use the `git checkout` command followed by the tag name.
---

**Contents**

[TOC]

### Step 1: Clone the Repository

Clone the repository to your local machine by running the following command:

```
git clone <repository-url>
```

### Step 2: Check Out the Tag

Check out the tag by running the following command:

```
git checkout <tag-name>
```

### Step 3: Pull the Tag

Pull the tag by running the following command:

```
git pull origin <tag-name>
```

### Step 4: Verify the Tag

Verify the tag by running the following command:

```
git tag -v <tag-name>
```
