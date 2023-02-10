---
title: Printing JSON in a formatted way with react
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: React provides the <pre> tag to render and style JSON data in a human-readable format.
---

**Contents**

[TOC]

#### Section 1: Setting up React

To get started, you will need to install React and create a React app. To do this, you can use the create-react-app command line tool. This will create a new React project and install all the necessary dependencies.

#### Section 2: Importing the JSON

Once you have created your React project, you will need to import the JSON file into your project. This can be done by using the import keyword. For example:

```javascript
import jsonData from './myJson.json';
```

#### Section 3: Rendering the JSON

Once you have imported the JSON data, you can render it using the React component. You can use the map() method to iterate over the JSON data and render it in the component. For example:

```javascript
render() {
  return (
    <div>
      {jsonData.map(item => (
        <div>
          <p>{item.name}</p>
          <p>{item.age}</p>
        </div>
      ))}
    </div>
  );
}
```

#### Section 4: Pretty Printing the JSON

Finally, you can use the JSON.stringify() method to pretty print the JSON data. This will format the JSON data in a readable way. For example:

```javascript
const prettyJson = JSON.stringify(jsonData, null, 2);
```

The second argument is used to specify the number of spaces to indent the JSON data. In this case, we are using 2 spaces.
