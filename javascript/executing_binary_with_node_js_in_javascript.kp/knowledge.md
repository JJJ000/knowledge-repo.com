---
title: Run a command line binary using node.js
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Node.js can execute a command line binary with the `child\_process` module`s `exec()` method.
---

**Contents**

[TOC]

# Using Child Process

The `child_process` module provides the ability to execute a command line binary with Node.js. It provides a variety of methods for creating child processes, including `spawn()`, `exec()`, and `execFile()`.

## spawn()

The `spawn()` method launches a new process with the given command, with command line arguments in an array. It returns a `ChildProcess` object, which can be used to access the process's stdin, stdout, and stderr.

Example:

```javascript
const { spawn } = require('child_process');

const ls = spawn('ls', ['-lh', '/usr']);

ls.stdout.on('data', (data) => {
  console.log(`stdout: ${data}`);
});

ls.stderr.on('data', (data) => {
  console.log(`stderr: ${data}`);
});

ls.on('close', (code) => {
  console.log(`child process exited with code ${code}`);
});
```

## exec()

The `exec()` method executes a command in a shell and buffers the output. It takes a single string argument containing the command to execute, and returns a `ChildProcess` object.

Example:

```javascript
const { exec } = require('child_process');

exec('ls -lh /usr', (err, stdout, stderr) => {
  if (err) {
    console.error(`exec error: ${err}`);
    return;
  }
  console.log(`stdout: ${stdout}`);
  console.log(`stderr: ${stderr}`);
});
```

## execFile()

The `execFile()` method is similar to `exec()`, but it does not spawn a shell. Instead, it executes the specified file directly, with command line arguments in an array. It takes a single string argument containing the path to the file to execute, and returns a `ChildProcess` object.

Example:

```javascript
const { execFile } = require('child_process');

execFile('ls', ['-lh', '/usr'], (err, stdout, stderr) => {
  if (err) {
    console.error(`execFile error: ${err}`);
    return;
  }
  console.log(`stdout: ${stdout}`);
  console.log(`stderr: ${stderr}`);
});
```
