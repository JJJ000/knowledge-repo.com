---
title: Npm is warning that a peer dependency is required, but none is installed. you will need to install the peer dependency yourself
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You must manually install the required peer dependencies.
---

**Contents**

[TOC]

#### Installing Peer Dependencies 

1. Check the package.json file of the package that you are trying to install. This will list all of the peer dependencies that you will need to install. 

2. Install the required peer dependencies using npm. For example, if you need to install the 'lodash' peer dependency, you would run the following command: 

```
npm install lodash
```

#### Verifying Peer Dependencies 

1. Check the package.json file of the package you are trying to install to make sure that all of the required peer dependencies are installed. 

2. You can also use the npm list command to verify that all of the peer dependencies are installed. This command will list all of the dependencies and peer dependencies of the package you are trying to install. 

#### Troubleshooting

1. If you are still getting the warning message after verifying that all of the peer dependencies are installed, you may need to uninstall and reinstall the package.

2. If the issue persists, it may be due to a version mismatch between the package and its peer dependencies. Try installing the exact version of the peer dependencies that are listed in the package.json file.
