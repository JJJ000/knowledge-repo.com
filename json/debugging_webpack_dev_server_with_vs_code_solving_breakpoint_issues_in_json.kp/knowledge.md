---
title: A guide on utilizing the vs code debugger with webpack-dev-server while ensuring that breakpoints are not being ignored
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Set the `sourceMap` property to true in the launch configuration of VS Code debugger.
---

**Contents**

[TOC]

# Introduction
In web development, we often use both VS Code and Webpack-dev-server for our work. However, as easy as it looks, debugging applications using the two tools could be quite challenging. This problem is especially pronounced when trying to add breakpoints to the code, but for some reasons, they don’t trigger. In this guide, we will walk you through some tips to help you successfully use VS Code debugger with webpack-dev-server.

# Steps to Use VS Code Debugger with Webpack-dev-server
Here are the steps to follow when trying to use VS Code debugger with webpack-dev-server.

## Step 1: Ensure appropriate script is present in your package.json

The first thing to check is to ensure that the script that launches your webpack-dev-server is present in the package.json file. Always ensure that the script is set to ‘dev.’ 

Example: 

```json
"scripts": {
    "dev": "webpack-dev-server --config webpack.config.json --progress --no-color --watch",
  },
```
  
## Step 2: Configure your launch.json for your project correctly
In your project folder, open the ‘launch.json’ file and ensure that you have the following configuration settings:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "chrome",
            "request": "launch",
            "name": "Launch in Chrome",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}/src",
            "sourceMapPathOverrides": {
                "webpack:///./*": "${webRoot}/*"
            }
        }
    ]
}
```

## Step 3: Configure your webpack.config.js correctly
In your navigator, locate your main ‘webpack.config.js’ file and ensure the following changes are made:

```json
 devtool: 'source-map',
  devServer: {

    contentBase: path.join(__dirname, 'dist'),
    compress: true,
    port: 8080,
    stats: 'errors-only',
    hot: true,
    open: true,
  },
```

Ensure that you set your devtool to ‘source-map’, and it’s also advisable to enable hot-reloading to make the debugging process more seamless.

## Step 4: Launch webpack-dev-server on VS Code
The final step is to launch the webpack-dev-server on VS Code via the following steps:

1. Click on the Debugging button on the left side of the screen.
2. From the dropdown options click on the ‘Launch in Chrome’ option.
3. Debugger will launch the Chrome browser, which will open your application using webpack-dev-server at http://localhost:8080.
4. Set breakpoints in your code, and the debugger will then pause when the code runs.

# Conclusion
Debugging with Webpack-dev-server and VS Code work best when you have set things up correctly from the beginning. Following the above tips will help you set up everything correctly, and you will spend less time on debugging and finding issues in your code.
