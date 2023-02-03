---
title: Passing command line arguments to an npm script
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can pass command line arguments to an npm script by using the `--` flag followed by the argument.
---

**Contents**

[TOC]

**Section 1: Overview**

Npm scripts are a way to execute commands and run scripts defined in a package.json file. They are often used to run tasks such as building a project, running tests, or deploying an application. Passing command line arguments to npm scripts allows developers to customize their scripts and control how the script runs.

**Section 2: Setting Up the Script**

To pass command line arguments to an npm script, first set up the script in the package.json file. The script should include a placeholder for the argument, such as `$1`. This placeholder will be replaced by the argument when the script is run.

**Section 3: Running the Script**

To run the script with a command line argument, use the `--` flag followed by the argument. For example, if the script is named `myScript` and the argument is `myArgument`, the command would be `npm run myScript -- myArgument`.

**Section 4: Using the Argument**

Once the argument has been passed to the script, it can be used in the script code. The argument can be accessed using the `process.argv` array, which contains the command line arguments. The first argument is always the script name, so the argument will be at index 2. For example, if the argument is `myArgument`, the code to access it would be `process.argv[2]`.
