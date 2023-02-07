---
title: Execute a node js script's function from the command line
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can run a script from the command line in Node JS by using the `node` command followed by the script file name.
---

**Contents**

[TOC]

# Setup

To run a script from the command line in Node JS, you will need to first install Node.js on your system. You can find instructions for installing Node.js on the [Node.js website](https://nodejs.org/en/).

# Running a Script

Once Node.js is installed, you can run a script by navigating to the directory containing the script and running the following command:

```
node <script-name>.js
```

Where `<script-name>` is the name of the script you want to run.

# Passing Arguments

You can also pass arguments to the script when running it from the command line. For example, if you wanted to pass two arguments to a script named `myScript.js`, you could run the following command:

```
node myScript.js arg1 arg2
```

# Output

The output of the script will be printed to the console.
