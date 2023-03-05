---
title: What is the method to incorporate boon or Jackson JSON parsers in an Android project using gradle?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Add the following dependencies to your app-level build.gradle file implementation `com.fasterxml.jackson.corejackson-core2.12.3` and implementation `org.boonboon-core0.35`.
---

**Contents**

[TOC]

## Adding Boon JSON parser to Android project with Gradle

Boon is a high-performance JSON parser for Java. Here are the steps to add Boon JSON parser to your Android project with Gradle.

1. Open your `build.gradle` file, which should look something like this:

   ```groovy
   apply plugin: 'com.android.application'

   android {
       // ...
   }

   dependencies {
       // ...
   }
   ```

2. Add the `boon-json` dependency to the `dependencies` block:

   ```groovy
   apply plugin: 'com.android.application'

   android {
       // ...
   }

   dependencies {
       // ...
       implementation 'io.fastjson:boon-json:0.32'
   }
   ```

3. Sync your Gradle project to download the new dependencies.

4. That's it! You can now use the Boon JSON parser in your Android project.


## Adding Jackson JSON parser to Android project with Gradle

Jackson is a popular JSON parser for Java. Here's how you can add it to your Android project with Gradle:

1. Open your `build.gradle` file.

2. Add the `jackson-core` and `jackson-databind` dependencies to the `dependencies` block:

   ```groovy
   apply plugin: 'com.android.application'

   android {
       // ...
   }

   dependencies {
       // ...
       implementation 'com.fasterxml.jackson.core:jackson-core:2.12.3'
       implementation 'com.fasterxml.jackson.core:jackson-databind:2.12.3'
   }
   ```

3. Sync your Gradle project to download the new dependencies.

4. That's it! You can now use the Jackson JSON parser in your Android project.

## Usage example

Once you have added either Boon or Jackson JSON parser to your Android project, you can use it to parse JSON data as follows:

```java
import com.fasterxml.jackson.databind.ObjectMapper;
import io.advantageous.boon.json.JsonFactory;
import io.advantageous.boon.json.ObjectMapperFactory;

// ...

ObjectMapper mapper = new ObjectMapper(); // for Jackson
JsonFactory factory = new JsonFactory(); // for Boon
ObjectMapperFactory objectMapperFactory = new ObjectMapperFactory(); // for Boon

// Parsing JSON with Jackson
MyObject obj = mapper.readValue(jsonString, MyObject.class);

// Parsing JSON with Boon
MyObject obj = factory.create().fromJson(jsonString, MyObject.class);
MyObject obj = objectMapperFactory.create().fromJson(jsonString, MyObject.class);
```

Replace `MyObject` with the name of the class that represents the JSON data you want to parse. `jsonString` is a `String` variable containing the JSON data you want to parse.
