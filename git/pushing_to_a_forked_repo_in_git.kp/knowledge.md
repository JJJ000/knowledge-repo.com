---
title: What is the process for pushing changes from a clone of the original repository to my fork?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can push to your fork from a clone of the original repo by using the `git push` command.
---

**Contents**

[TOC]

# Step 1: Add Remote

First, you need to add the original repository as a remote to your cloned repository. This allows you to access the original repository from your clone. To do this, use the following command:

`git remote add upstream <url_of_original_repo>`

# Step 2: Fetch Content

Next, you need to fetch the content from the original repository to your clone. This will allow you to access the latest changes from the original repository. To do this, use the following command:

`git fetch upstream`

# Step 3: Merge Changes

Now, you need to merge the changes from the original repository into your clone. This will ensure that your clone is up to date with the original repository. To do this, use the following command:

`git merge upstream/master`

# Step 4: Push Changes

Finally, you need to push the changes from your clone to your fork. This will ensure that your fork is up to date with the original repository. To do this, use the following command:

`git push origin master`
