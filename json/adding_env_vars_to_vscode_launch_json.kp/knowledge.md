---
title: What is the process for adding environment variables to launch.json in vscode?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Add an `env` object to the `configurations` array in launch.json.
---

**Contents**

[TOC]

## Step 1: Access launch.json
1. Open the Command Palette in VSCode (Ctrl + Shift + P).
2. Type in "Debug: Open launch.json" and press enter.

## Step 2: Add Environment Variables
1. In launch.json, add the following line: 
```
"env": { "VARIABLE_NAME": "value" }
```
2. Replace "VARIABLE_NAME" with the name of the environment variable you want to add and "value" with the value you want to assign to the variable.
3. Repeat this step for each environment variable you want to add.

## Step 3: Save Changes
1. Save the changes made to launch.json by pressing Ctrl + S.
2. The environment variables will now be available in your VSCode workspace.
