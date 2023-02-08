---
title: How can I prevent specific fields from being serialized with gson without using annotations?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can exclude specific fields from serialization by using the Gson ExclusionStrategy interface.
---

**Contents**

[TOC]

## Excluding Specific Fields with Gson

Gson provides several options for excluding specific fields from serialization without the need for annotations.

### Using ExclusionStrategies

The most straightforward way to exclude fields from serialization is to use an ExclusionStrategy. An ExclusionStrategy is an interface that allows you to specify which fields should be excluded from serialization. To use an ExclusionStrategy, you must first create an instance of the ExclusionStrategy. Then, you can pass the ExclusionStrategy to the GsonBuilder when creating a Gson instance.

For example, if you wanted to exclude all fields that are marked as `transient`, you could create an ExclusionStrategy like this:

```java
ExclusionStrategy transientExclusionStrategy = new ExclusionStrategy() {
    @Override
    public boolean shouldSkipField(FieldAttributes f) {
        return f.isTransient();
    }

    @Override
    public boolean shouldSkipClass(Class<?> clazz) {
        return false;
    }
};
```

Then, you can pass the ExclusionStrategy to the GsonBuilder when creating a Gson instance:

```java
Gson gson = new GsonBuilder()
    .setExclusionStrategies(transientExclusionStrategy)
    .create();
```

### Using GsonBuilder.excludeFieldsWithoutExposeAnnotation

Another way to exclude fields from serialization is to use the `GsonBuilder.excludeFieldsWithoutExposeAnnotation` method. This method instructs Gson to exclude all fields that are not marked with the `@Expose` annotation.

To use this method, you must first create a GsonBuilder instance. Then, you can call the `excludeFieldsWithoutExposeAnnotation` method on the GsonBuilder instance. Finally, you can create a Gson instance from the GsonBuilder.

For example:

```java
Gson gson = new GsonBuilder()
    .excludeFieldsWithoutExposeAnnotation()
    .create();
```

### Using GsonBuilder.addSerializationExclusionStrategy

The `GsonBuilder.addSerializationExclusionStrategy` method allows you to specify an ExclusionStrategy for serialization. This method is similar to the `GsonBuilder.setExclusionStrategies` method, but it only applies to serialization.

To use this method, you must first create a GsonBuilder instance. Then, you can call the `addSerializationExclusionStrategy` method on the GsonBuilder instance. Finally, you can create a Gson instance from the GsonBuilder.

For example:

```java
Gson gson = new GsonBuilder()
    .addSerializationExclusionStrategy(transientExclusionStrategy)
    .create();
```
