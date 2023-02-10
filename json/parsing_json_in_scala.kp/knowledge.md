---
title: What are the standard scala classes for parsing JSON in scala?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the scala.util.parsing.json.JSON library to parse JSON in Scala using standard Scala classes.
---

**Contents**

[TOC]

### Section 1: Setup

In order to parse JSON in Scala, you need to have the `json4s` library installed. This can be done by adding the following to your `build.sbt` file:

```
libraryDependencies += "org.json4s" %% "json4s-native" % "3.5.3"
```

### Section 2: Importing the Library

Once the `json4s` library is installed, you can import it into your Scala code:

```
import org.json4s._
import org.json4s.native.JsonMethods._
```

### Section 3: Parsing the JSON

You can then parse the JSON by using the `parse` method:

```
val jsonString = """{"name": "John Doe", "age": 42}"""
val parsedJson = parse(jsonString)
```

### Section 4: Accessing the Data

Once the JSON is parsed, you can access the data in the JSON object using the `\` operator:

```
val name = (parsedJson \ "name").extract[String]
val age = (parsedJson \ "age").extract[Int]
```
