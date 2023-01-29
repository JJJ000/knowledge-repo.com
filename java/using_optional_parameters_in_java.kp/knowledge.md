---
title: What is the syntax for using optional parameters in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Optional parameters in Java can be used by declaring parameters as optional within the method signature and providing default values for them.
---

**Contents**

[TOC]

### Defining Optional Parameters

Optional parameters are parameters that can be included in a function call, but are not required. In Java, optional parameters are implemented using the `java.util.Optional` class. 

### Creating Optional Objects

To create an `Optional` object, you can use the `Optional.of()` method. This method takes a single parameter which is the value that is wrapped in the `Optional` object. 

```java
Optional<String> optionalString = Optional.of("My String");
```

You can also create an empty `Optional` object using the `Optional.empty()` method.

```java
Optional<String> optionalString = Optional.empty();
```

### Using Optional Parameters

When defining a function, you can use an `Optional` object as a parameter to make it optional. 

```java
public void myFunction(String requiredParam, Optional<String> optionalParam){
    // function logic
}
```

When calling the function, you can either pass in a value for the optional parameter or simply leave it out. 

```java
// Passing in an optional parameter
myFunction("requiredParam", Optional.of("optionalParam"));

// Not passing in an optional parameter
myFunction("requiredParam");
```

### Checking for Optional Parameters

When using an optional parameter in a function, you may need to check if a value was passed in or not. To do this, you can use the `Optional.isPresent()` method. 

```java
public void myFunction(String requiredParam, Optional<String> optionalParam){
    if(optionalParam.isPresent()){
        // optional parameter was passed in
    } else {
        // optional parameter was not passed in
    }
}
```
