---
title: Modify a commit message in sourcetree on windows that has already been pushed to the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: It is not possible to edit a commit message in SourceTree Windows after it has been pushed to a remote.
---

**Contents**

[TOC]

# Step 1: Revert to the Previous Commit

1. In SourceTree, right-click on the commit you want to change and select "Revert <Commit SHA>". 

2. A new commit will be created to revert the changes made in the original commit.

# Step 2: Amend the Commit

1. Right-click on the new commit and select "Amend Last Commit".

2. This will open up the commit message editor where you can edit the commit message.

# Step 3: Push the Changes

1. Once you have finished editing the commit message, click the "Commit" button.

2. Push the changes to the remote repository.
