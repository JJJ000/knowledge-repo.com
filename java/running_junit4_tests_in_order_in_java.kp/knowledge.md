---
title: What is the best way to order the execution of test methods in junit4?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In JUnit4, tests can be run in a specific order by annotating them with @FixMethodOrder and specifying the MethodSorters.
---

**Contents**

[TOC]

### Using @FixMethodOrder Annotation

JUnit 4 provides the @FixMethodOrder annotation to control the order of test methods. The annotation takes a value of type org.junit.runners.MethodSorters which provides four different options to sort the test methods:

1. MethodSorters.DEFAULT: This is the default behavior and test methods are sorted alphabetically.

2. MethodSorters.NAME_ASCENDING: This will sort the test methods in an ascending order based on their names.

3. MethodSorters.JVM: This will sort the test methods based on the order in which the JVM has stored them.

4. MethodSorters.RANDOM: This will sort the test methods in a random order.

To use the @FixMethodOrder annotation, we need to add it to our test class. For example:

@FixMethodOrder(MethodSorters.NAME_ASCENDING)
public class MyTestClass {
    // Test methods
}

### Using @Test Annotation

The @Test annotation also provides an optional parameter called “expected” which can be used to specify the expected exception type that a test method should throw. This parameter can also be used to control the order of test methods.

To use this approach, we need to specify the expected exception type for each test method in the order in which we want them to be executed. For example:

@Test(expected = IllegalArgumentException.class)
public void testMethod1() {
    // Test method
}

@Test(expected = NullPointerException.class)
public void testMethod2() {
    // Test method
}

### Using TestSuite

The TestSuite class provides a way to specify the order in which test methods should be executed. We can create a TestSuite object and add test methods to it in the order in which we want them to be executed. For example:

TestSuite suite = new TestSuite();
suite.addTest(new MyTestClass("testMethod1"));
suite.addTest(new MyTestClass("testMethod2"));

### Using TestRule

JUnit also provides a TestRule interface which can be used to control the order of test methods. We can create a custom TestRule implementation and add it to our test class. This TestRule can then be used to control the order of test methods. For example:

public class MyTestClass {
    @Rule
    public TestRule myTestRule = new MyTestRule();

    // Test methods
}

public class MyTestRule implements TestRule {
    @Override
    public Statement apply(final Statement base, Description description) {
        // Logic to control the order of test methods
    }
}
