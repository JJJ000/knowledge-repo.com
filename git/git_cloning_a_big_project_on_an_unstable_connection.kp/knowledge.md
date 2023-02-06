---
title: What steps should I take to successfully clone a large project from a git repository over an unreliable internet connection?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `--depth` flag to limit the amount of data downloaded during the clone.
---

**Contents**

[TOC]

# Section 1: Prepare for the Clone
1. Check the size of the repository you are cloning.
2. Ensure that you have a stable internet connection with sufficient bandwidth to handle the size of the repository.
3. Create a local directory to store the repository.

# Section 2: Start the Clone
1. Open a terminal window and navigate to the local directory.
2. Run the command `git clone <url>` to start the clone.

# Section 3: Monitor the Clone
1. Monitor the progress of the clone.
2. Check the connection status and bandwidth usage.

# Section 4: Resume the Clone
1. If the connection is lost, resume the clone by running the command `git clone --resume <url>`.
2. Monitor the progress of the clone and check the connection status and bandwidth usage.
