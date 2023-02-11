---
title: Using jsoncreator, what is the process for deserializing a class with multiple constructors?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the @JsonCreator annotation to specify which constructor to use when deserializing the class.
---

**Contents**

[TOC]

### Solution 1

#### Step 1: Annotate the Constructors

The first step to deserializing a class with overloaded constructors is to annotate the constructors with the `@JsonCreator` annotation. This will tell Jackson to use the annotated constructor when deserializing the class.

#### Step 2: Annotate the Constructor Parameters

The next step is to annotate the constructor parameters with `@JsonProperty` annotation. This will tell Jackson which parameters should be used when deserializing the class.

#### Step 3: Create a Custom Deserializer

If the class has complex logic that needs to be applied when deserializing, then it is necessary to create a custom deserializer. This will allow you to apply the logic when deserializing the class.

### Solution 2

#### Step 1: Annotate the Constructors

The first step to deserializing a class with overloaded constructors is to annotate the constructors with the `@JsonCreator` annotation. This will tell Jackson to use the annotated constructor when deserializing the class.

#### Step 2: Annotate the Constructor Parameters

The next step is to annotate the constructor parameters with `@JsonProperty` annotation. This will tell Jackson which parameters should be used when deserializing the class.

#### Step 3: Use the @JsonCreator Factory Method

If the class has complex logic that needs to be applied when deserializing, then it is possible to use the `@JsonCreator` factory method. This will allow you to apply the logic when deserializing the class.

#### Step 4: Register the Custom Deserializer

Finally, it is necessary to register the custom deserializer with the Jackson ObjectMapper. This will tell Jackson to use the custom deserializer when deserializing the class.
