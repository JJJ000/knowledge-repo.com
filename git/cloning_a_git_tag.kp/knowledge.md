---
title: How to create a copy of a specific git tag
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To clone a specific Git tag, use the command `git clone -b <tag\_name> <repository\_url>`.
---

**Contents**

[TOC]

### 1. Install Git
First, you need to install Git on your computer. Git is available for Windows, Mac, and Linux.

### 2. Find the Tag
Next, you need to find the specific tag you want to clone. You can use a Git repository browser such as GitHub or GitLab to find the tag.

### 3. Clone the Tag
Once you have found the tag, you can clone it using the following command:

`git clone -b <tag_name> <repository_url>`

### 4. Check Out the Tag
Finally, you can check out the tag using the following command:

`git checkout <tag_name>`
