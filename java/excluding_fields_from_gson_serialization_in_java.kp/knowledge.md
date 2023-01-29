---
title: How to prevent certain fields from being serialized with gson without using annotations?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is possible to exclude specific fields from serialization without annotations in Java by using the GsonBuilder.excludeFieldsWithoutExposeAnnotation() method.
---

**Contents**

[TOC]

### Option 1 - Exclude fields from Serialization explicitly

It is possible to exclude fields from serialization explicitly by using the `GsonBuilder.excludeFieldsWithoutExposeAnnotation()` method. This method takes an array of `Class` objects and excludes all fields that do not have the `@Expose` annotation.

```java
Gson gson = new GsonBuilder()
    .excludeFieldsWithoutExposeAnnotation()
    .create();
```

### Option 2 - Exclude fields from Serialization using a custom ExclusionStrategy

It is possible to exclude fields from serialization by implementing a custom `ExclusionStrategy` and registering it with a `GsonBuilder` instance. The `shouldSkipField()` method of the `ExclusionStrategy` will be called for each field in the object and can be used to determine if the field should be excluded from serialization.

```java
Gson gson = new GsonBuilder()
    .setExclusionStrategy(new ExclusionStrategy() {
        public boolean shouldSkipField(FieldAttributes f) {
            return f.getName().equals("fieldNameToExclude");
        }

        public boolean shouldSkipClass(Class<?> clazz) {
            return false;
        }
    })
    .create();
```

### Option 3 - Exclude fields from Serialization using a TypeAdapter

It is possible to exclude fields from serialization by implementing a custom `TypeAdapter` and registering it with a `GsonBuilder` instance. The `write()` method of the `TypeAdapter` will be called for each field in the object and can be used to determine if the field should be excluded from serialization.

```java
Gson gson = new GsonBuilder()
    .registerTypeAdapter(MyClass.class, new TypeAdapter<MyClass>() {
        public void write(JsonWriter out, MyClass value) throws IOException {
            out.beginObject();
            out.name("fieldNameToInclude");
            out.value(value.fieldNameToInclude);
            out.endObject();
        }

        public MyClass read(JsonReader in) throws IOException {
            // Implement read() if needed
        }
    })
    .create();
```

### Option 4 - Exclude fields from Serialization using a RuntimeTypeAdapterFactory

It is possible to exclude fields from serialization by using a `RuntimeTypeAdapterFactory` and registering it with a `GsonBuilder` instance. The `RuntimeTypeAdapterFactory` can be used to exclude fields from a specific type or subtype.

```java
RuntimeTypeAdapterFactory<MyClass> factory = RuntimeTypeAdapterFactory
    .of(MyClass.class, "type")
    .registerSubtype(MySubclass.class, "subtype")
    .excludeField(MySubclass.class, "fieldNameToExclude");

Gson gson = new GsonBuilder()
    .registerTypeAdapterFactory(factory)
    .create();
```
