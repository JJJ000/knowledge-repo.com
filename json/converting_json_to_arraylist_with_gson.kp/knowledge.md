---
title: Convert a JSON string into an arraylist of a specific type using gson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Gson can be used to deserialize a JSON string into an ArrayList of a specified type.
---

**Contents**

[TOC]

**Section 1: Add Dependencies**

To use Gson, you must add the Gson library as a dependency to your project. This can be done with Gradle or Maven, depending on your project setup.

**Section 2: Create a Gson Object**

Once the Gson library is added, you can create a Gson object. You can do this with the following code:

```
Gson gson = new Gson();
```

**Section 3: Convert Json to ArrayList<T>**

Once you have a Gson object, you can use the fromJson() method to convert a JSON string to an ArrayList<T> object. The syntax for this is as follows:

```
ArrayList<T> list = gson.fromJson(jsonString, new TypeToken<ArrayList<T>>(){}.getType());
```

Where jsonString is the JSON string to be converted, and T is the type of the elements in the ArrayList.

**Section 4: Example**

For example, if you have a JSON string that looks like this:

```
[{"name": "John", "age": 30}, {"name": "Jane", "age": 25}]
```

And you want to convert it to an ArrayList of Person objects, you could do the following:

```
Gson gson = new Gson();
ArrayList<Person> list = gson.fromJson(jsonString, new TypeToken<ArrayList<Person>>(){}.getType());
```
