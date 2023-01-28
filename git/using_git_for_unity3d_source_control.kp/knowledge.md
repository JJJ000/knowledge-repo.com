---
title: What are the steps for using git for unity3d source control?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To use Git for Unity3D source control, you must first initialize a local Git repository and then link it to a remote repository (e.g. GitHub).
---

**Contents**

[TOC]

### Step 1: Set up a Git Repository

1. Create a new repository on GitHub or other online Git hosting service.
2. Clone the repository to your local machine.
3. Add the Unity project to the repository.

### Step 2: Configure Unity

1. Open the Unity project.
2. Go to Edit > Project Settings > Editor.
3. Under Version Control, select “Visible Meta Files”.
4. Under Asset Serialization, select “Force Text”.

### Step 3: Commit and Push Changes

1. Make changes to the project.
2. In the Unity editor, go to Assets > Sync MonoDevelop Project.
3. Open the terminal, navigate to the repository directory, and commit the changes.
4. Push the changes to the remote repository.

### Step 4: Pull Changes from the Remote Repository

1. Open the terminal, navigate to the repository directory.
2. Pull the changes from the remote repository.
3. In the Unity editor, go to Assets > Sync MonoDevelop Project.
