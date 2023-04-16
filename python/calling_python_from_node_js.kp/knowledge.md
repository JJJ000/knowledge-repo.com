---
title: What is the process for invoking a Python function from node.js?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Node.js can call a Python function by using the `child\_process` module to spawn a Python process and pass the function call as an argument.
---

**Contents**

[TOC]

# Section 1: Install Python Module

The first step to call a Python function from Node.js is to install a Python module. The most popular module for this purpose is the `python-shell` module. This module can be installed using npm as follows:

```
npm install python-shell
```

# Section 2: Configure Python Path

The `python-shell` module requires the path to the Python executable to be configured. This can be done by setting the `pythonPath` option in the `PythonShell` constructor. For example:

```
const PythonShell = require('python-shell');
const options = {
    pythonPath: '/usr/bin/python3'
};
const pyshell = new PythonShell('my_script.py', options);
```

# Section 3: Call Python Function

Once the `PythonShell` object is created, the `run` method can be used to call the Python function. This method takes two arguments: the first argument is the name of the Python script to be executed, and the second argument is an object containing the parameters to be passed to the Python script. For example:

```
const args = {
    param1: 'value1',
    param2: 'value2'
};
pyshell.run('my_script.py', args, function (err, results) {
    if (err) throw err;
    // results is an array consisting of messages collected during execution 
    console.log('results: %j', results);
});
```

# Section 4: Handle Results

The `run` method returns an array of messages collected during execution. The results of the Python script can be accessed from this array. For example, if the Python script prints a message, the output can be accessed from the array as follows:

```
const output = results[0];
console.log(output);
```
