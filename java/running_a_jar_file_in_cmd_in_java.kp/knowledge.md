---
title: Execute a jar file using the command line
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To run a jar file in command prompt, use the command `java -jar <jar-file-name>.jar`.
---

**Contents**

[TOC]

### Step 1: Navigate to the Directory

First, you need to navigate to the directory where the jar file is located. You can use the `cd` command to change directories. For example, if the jar file is located in the `C:\Program Files\MyProgram` directory, you can use the following command to navigate to it:

`cd C:\Program Files\MyProgram`

### Step 2: Execute the Jar File

Once you are in the directory containing the jar file, you can execute it using the following command:

`java -jar <filename>.jar`

Replace `<filename>` with the name of the jar file.

### Step 3: Provide Arguments (Optional)

If the jar file requires any arguments, you can provide them after the jar file name. For example:

`java -jar <filename>.jar arg1 arg2 arg3`

### Step 4: View the Output

Once the jar file has been executed, the output will be displayed in the command prompt window.
