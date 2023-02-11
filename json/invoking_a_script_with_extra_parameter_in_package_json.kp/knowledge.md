---
title: In node package.json, call a script from another script with an additional argument, for example, start a mocha watcher
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can use the `--` flag to pass extra parameters to a script when invoking it from another script in package.json.
---

**Contents**

[TOC]

**Section 1: Invoking script from another script**

In package.json, you can invoke a script from another script by specifying the script name in the "scripts" section of the package.json file. For example, if you have a script named "test" and you want to invoke it from another script, you can do so by adding the following line to the "scripts" section of the package.json file:

"test": "node test.js"

**Section 2: Adding an extra parameter**

In order to add an extra parameter to the script you are invoking, you can use the "--" syntax. For example, if you wanted to add a mocha watcher to the script, you could do so by adding the following line to the "scripts" section of the package.json file:

"test": "node test.js -- --watch"

**Section 3: Using the npm run command**

Once you have added the extra parameter to the script, you can then invoke the script using the npm run command. For example, if you wanted to invoke the test script with the mocha watcher, you could do so by running the following command:

npm run test -- --watch

**Section 4: Verifying the results**

Once you have invoked the script with the extra parameter, you can verify that the mocha watcher is running by running the following command:

mocha --watch

This command will list all of the tests that are being watched by the mocha watcher.
