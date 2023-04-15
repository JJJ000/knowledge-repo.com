---
title: Having the mocked method return the same argument that was given to it
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The mocked method can return the argument passed to it by using the `Answer.returnArg()` syntax.
---

**Contents**

[TOC]

`**` Setting Up the Mocked Method**

The first step is to create a Mockito mock object of the class that contains the method you want to mock. This can be done with the Mockito.mock() method.

```
MyClass mockedMyClass = Mockito.mock(MyClass.class);
```

`**` Defining the Mock Method**

Next, you need to define the behavior of the mocked method. This is done using the Mockito.when() method.

```
Mockito.when(mockedMyClass.myMethod(ArgumentMatchers.any())).thenAnswer(invocation -> {
    return invocation.getArgument(0);
});
```

`**` Invoking the Mock Method**

Finally, you need to invoke the mocked method. This is done by calling the method on the mocked object.

```
Object result = mockedMyClass.myMethod("my argument");
```

`**` Verifying the Result**

To verify that the mocked method is returning the argument that was passed to it, you can use the Mockito.verify() method.

```
Mockito.verify(mockedMyClass).myMethod("my argument");
```
