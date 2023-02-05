---
title: Store the output of os.system in a variable without printing it to the console
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: output = os.system(`command`) can be used to assign the output of os.system to a variable, while the `>/dev/null 2>&1` argument can be added to the end of the command to prevent it from being displayed on the screen.
---

**Contents**

[TOC]

# Using Subprocess

## Step 1: Import Subprocess

```python
import subprocess
```

## Step 2: Create a Variable to Store the Output

```python
output = subprocess.PIPE
```

## Step 3: Call os.system with the Output Variable

```python
os.system('command', stdout=output)
```

## Step 4: Store the Output in a Variable

```python
result = subprocess.run('command', stdout=output)
```
