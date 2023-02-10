---
title: What is the process for converting a list from JSON to Java using gson or another JSON library?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Using GSON, you can deserialize a list by calling the fromJson() method on a Gson instance, passing in the JSON string and the type of the list.
---

**Contents**

[TOC]

# Section 1: Add Gson Dependency

In order to use Gson, you need to add the Gson dependency to your project. To do this, add the following dependency to your `build.gradle` file:

```
implementation 'com.google.code.gson:gson:2.8.6'
```

# Section 2: Create Gson Object

Next, create a Gson object. This will be used to deserialize the JSON into a list.

```
Gson gson = new Gson();
```

# Section 3: Deserialize the JSON

Now you can use the Gson object to deserialize the JSON into a list.

```
List<Object> list = gson.fromJson(jsonString, new TypeToken<List<Object>>(){}.getType());
```

# Section 4: Iterate Through the List

Finally, you can iterate through the list and access the data.

```
for (Object obj : list) {
    // Access the data here
}
```
