---
title: What is the process for creating sourcemaps when using babel and webpack?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can generate sourcemaps by enabling the `devtool` option in your webpack configuration and adding the `sourceMap` option to your babel configuration.
---

**Contents**

[TOC]

### Step 1: Install Dependencies

Install `babel-loader` and `source-map-loader`:

```
npm install --save-dev babel-loader source-map-loader
```

### Step 2: Configure Webpack

In your webpack configuration file, add the following loader configuration:

```javascript
module: {
    rules: [
        {
            test: /\.js$/,
            exclude: /node_modules/,
            use: {
                loader: 'babel-loader',
                options: {
                    sourceMap: true,
                },
            },
        },
        {
            test: /\.js$/,
            enforce: 'pre',
            exclude: /node_modules/,
            use: {
                loader: 'source-map-loader',
            },
        },
    ],
},
```

### Step 3: Configure Babel

In your `.babelrc` file, add the following configuration:

```json
{
    "presets": ["@babel/preset-env"],
    "sourceMaps": true
}
```

### Step 4: Compile with Webpack

Finally, run your webpack build to generate the sourcemaps:

```
webpack --mode=development
```
