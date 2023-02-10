---
title: Importing JSON data from a local file into react js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the Fetch API to load JSON data from a local file into React JS.
---

**Contents**

[TOC]

#1. Setting up the File

First, create a file in your project directory and name it as `data.json`. In the file, paste the following code:

```
{
  "items": [
    {
      "id": 1,
      "name": "Item 1"
    },
    {
      "id": 2,
      "name": "Item 2"
    }
  ]
}
```

#2. Using the Fetch API

In your React component, import the `fetch` API:

```js
import { fetch } from 'whatwg-fetch';
```

Then, use the `fetch` API to get the data from the `data.json` file:

```js
fetch('data.json')
  .then(response => response.json())
  .then(data => {
    // do something with the data
  });
```

#3. Parsing the Data

Once the data is fetched, you can parse it and use it in your React component:

```js
fetch('data.json')
  .then(response => response.json())
  .then(data => {
    // parse the data
    const items = data.items.map(item => {
      return {
        id: item.id,
        name: item.name
      };
    });

    // use the data in the component
    this.setState({ items });
  });
```

#4. Rendering the Data

Finally, you can render the data in your React component:

```js
render() {
  return (
    <div>
      {this.state.items.map(item => (
        <div key={item.id}>{item.name}</div>
      ))}
    </div>
  );
}
```
