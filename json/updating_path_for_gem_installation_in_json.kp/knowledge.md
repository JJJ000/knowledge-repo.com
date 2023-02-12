---
title: In order to install the gem JSON version 1.7.3, you must ensure that your path includes the necessary build tools
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You need to add build tools to your PATH in order to install the JSON gem.
---

**Contents**

[TOC]

## Solution

### Update Your Path 
In order to install the json gem, you must first update your PATH to include build tools. This can be done by running the following command in your terminal: 

```
export PATH="/usr/local/bin:$PATH"
```

### Install the Gem
Once your PATH is updated, you can install the json gem with the following command: 

```
gem install json -v 1.7.3
```

### Verify Installation 
You can verify that the gem is installed correctly by running the following command: 

```
gem list
```

This will list all of the gems installed on your system. If the json gem is listed, it has been installed correctly.
