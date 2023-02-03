---
title: What is the best way to execute multiple npm scripts at the same time?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can use a package like npm-run-all to run multiple npm scripts in parallel.
---

**Contents**

[TOC]

# Section 1: Using npm-run-all

The easiest way to run multiple npm scripts in parallel is by using the npm-run-all package. This package allows you to specify multiple scripts to run in parallel with a single command.

# Section 2: Installation

To install npm-run-all, open your terminal and run the following command:

`npm install npm-run-all --save-dev`

# Section 3: Usage

Once npm-run-all is installed, you can specify multiple scripts to run in parallel by using the following syntax:

`npm-run-all <script1> <script2> <script3>`

# Section 4: Example

For example, if you have two scripts named `build` and `serve`, you can run them in parallel by using the following command:

`npm-run-all build serve`
