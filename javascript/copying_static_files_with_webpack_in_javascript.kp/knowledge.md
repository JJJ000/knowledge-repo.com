---
title: What is the process for copying static files to a build directory using webpack?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Using the CopyWebpackPlugin, static files can be copied from a source directory to the build directory.
---

**Contents**

[TOC]

1. Install `copy-webpack-plugin`

To copy static files to the build directory with Webpack, you will need to install the `copy-webpack-plugin` package. This plugin allows you to copy files or directories from the context directory to the output directory during the Webpack build process.

2. Configure `copy-webpack-plugin`

Once the `copy-webpack-plugin` package is installed, you will need to configure the plugin in your Webpack configuration file. To do this, you will need to add a `plugins` array to your Webpack configuration and add a new instance of the `CopyWebpackPlugin` to the array.

3. Add Static Files to the `copy-webpack-plugin` Configuration

Once the `copy-webpack-plugin` is configured, you will need to add the static files that you want to copy to the build directory. You can do this by adding a `patterns` array to the `CopyWebpackPlugin` configuration and listing the source files and the destination directory for each file.

4. Run Webpack Build

Finally, you will need to run the Webpack build command to copy the static files to the build directory. Once the build is complete, the static files will be available in the specified destination directory.
