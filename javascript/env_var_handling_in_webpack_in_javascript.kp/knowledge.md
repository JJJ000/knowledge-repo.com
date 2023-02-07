---
title: Including environment-specific variables in webpack configuration
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Environment-dependent variables can be passed in webpack using the DefinePlugin plugin.
---

**Contents**

[TOC]

##### Using webpack.DefinePlugin
The webpack.DefinePlugin allows you to create global constants which can be configured at compile time. This is useful for allowing different behavior between development builds and release builds.

For example, to set a development-only constant called DEV_MODE to true:

```javascript
new webpack.DefinePlugin({
  DEV_MODE: JSON.stringify(true)
});
```

##### Using Environment Variables
You can also use environment variables in webpack. Environment variables are global variables that are available to the process running webpack.

For example, to set a development-only constant called DEV_MODE to true:

```javascript
new webpack.DefinePlugin({
  DEV_MODE: JSON.stringify(process.env.DEV_MODE)
});
```

##### Using a Configuration File
You can also use a configuration file to store environment-dependent variables. This is useful when you need to store more than just a few variables.

For example, to set a development-only constant called DEV_MODE to true:

```javascript
// config.js
module.exports = {
  DEV_MODE: true
};
```

```javascript
// webpack.config.js
const config = require('./config');

new webpack.DefinePlugin({
  DEV_MODE: JSON.stringify(config.DEV_MODE)
});
```

##### Using Command Line Arguments
You can also use command line arguments to pass environment-dependent variables to webpack.

For example, to set a development-only constant called DEV_MODE to true:

```javascript
// webpack.config.js
new webpack.DefinePlugin({
  DEV_MODE: JSON.stringify(process.env.DEV_MODE)
});
```

Then, when running webpack, you can pass the argument --env.DEV_MODE=true:

```
webpack --env.DEV_MODE=true
```
