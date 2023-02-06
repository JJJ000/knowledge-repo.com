---
title: Reverting a git bisect error
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Revert the last commit and run `git bisect reset` to undo a git bisect mistake.
---

**Contents**

[TOC]

## Step 1: Revert Bisect Commit

If you have identified the wrong commit with `git bisect`, you can revert the commit with `git revert`. This will undo the changes made in the commit, effectively resetting the repository to its state before the commit was made.

## Step 2: Reset Bisect

After reverting the commit, you will need to reset the `git bisect` session with `git bisect reset`. This will clear out the `git bisect` session and return the repository to its original state.

## Step 3: Resume Bisect

Once you have reset the `git bisect` session, you can resume the search for the correct commit with `git bisect start`. This will start a new `git bisect` session and you can continue your search for the correct commit.

## Step 4: Check Bisect Results

Finally, you can check the results of your `git bisect` session with `git bisect log`. This will show all of the commits that have been checked during the session and will help you verify that the correct commit has been identified.
