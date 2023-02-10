---
title: What is the process for retrieving data from a local JSON file in a react native application?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `fetch` API to request the data from the local JSON file.
---

**Contents**

[TOC]

# Section 1: Setting up the Local JSON File

1. Create a directory in the root of your project called `data`.
2. Create a file in the data directory called `data.json`.
3. Add your JSON data to the file and save it.

# Section 2: Importing the Local JSON File

1. Import the `data.json` file in the component where you want to use the data.

```js
import data from './data/data.json';
```

# Section 3: Accessing the Data

1. Access the data using the `data` variable.

```js
const myData = data.myData;
```

# Section 4: Rendering the Data

1. Use the `myData` variable to render the data in the component.

```js
<Text>{myData}</Text>
```
