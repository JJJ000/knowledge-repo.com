---
title: What steps should I take to resolve a git merge conflict using vimdiff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git mergetool` and select vimdiff as the merge tool to resolve the conflict with vimdiff.
---

**Contents**

[TOC]

# Step 1: Open the Conflicting File

To begin, open the conflicting file in vimdiff. This can be done by running the command `git mergetool` from the command line. This will launch vimdiff with the conflicting files side by side.

# Step 2: Identify the Conflicting Lines 

The conflicting lines will be highlighted in the vimdiff window. The lines that have been changed by each branch will be highlighted in different colors. This will make it easier to identify the conflicting lines. 

# Step 3: Resolve the Conflict

Once the conflicting lines have been identified, it is time to resolve the conflict. This can be done by manually editing the conflicting lines in vimdiff. The conflicting lines can be edited to include the changes from both branches. 

# Step 4: Save and Exit

Once the conflict has been resolved, save the file and exit vimdiff. This will complete the merge conflict resolution process.
