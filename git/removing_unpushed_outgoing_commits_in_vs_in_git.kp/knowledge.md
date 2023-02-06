---
title: What is the process for undoing an unsent commit in visual studio?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To remove an unpushed outgoing commit in Visual Studio in Git, use the `Reset` command.
---

**Contents**

[TOC]

# Section 1: Discard Unpushed Outgoing Commit
1. Open the Team Explorer window in Visual Studio.
2. Select the **Changes** tab.
3. Select the commit that you want to discard.
4. Click the **Discard** button.

# Section 2: Reset Local Repository
1. Open the Team Explorer window in Visual Studio.
2. Select the **Branches** tab.
3. Select the branch that contains the commit you want to discard.
4. Click the **Actions** drop-down button and select **Reset**.
5. Select the **Reset Type** to **Hard**.
6. Click the **Reset** button.

# Section 3: Push Reset to Remote Repository
1. Open the Team Explorer window in Visual Studio.
2. Select the **Branches** tab.
3. Select the branch that you reset.
4. Click the **Actions** drop-down button and select **Push**.
5. Select the **Force Push** checkbox.
6. Click the **Push** button.

# Section 4: Verify Unpushed Outgoing Commit Is Discarded
1. Open the Team Explorer window in Visual Studio.
2. Select the **Changes** tab.
3. Verify that the commit you wanted to discard is no longer visible.
