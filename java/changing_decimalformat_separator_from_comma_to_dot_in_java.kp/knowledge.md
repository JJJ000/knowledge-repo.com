---
title: What is the procedure for altering the decimalformat decimal separator from a comma to a period?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the DecimalFormatSymbols class to set the DecimalFormat`s decimal separator to a dot/point.
---

**Contents**

[TOC]

**Section 1: Introduction**

The DecimalFormat class in Java is used to format decimal numbers. By default, it uses the comma (,) character as the decimal separator. However, it is possible to change the decimal separator to a dot (.) or any other character. This tutorial explains how to do that. 

**Section 2: Using the DecimalFormatSymbols Class**

The DecimalFormatSymbols class can be used to set the decimal separator for the DecimalFormat class. The following code shows how to use it:

```
DecimalFormatSymbols symbols = new DecimalFormatSymbols();
symbols.setDecimalSeparator('.');
DecimalFormat format = new DecimalFormat("#.##", symbols);
```

**Section 3: Using the setDecimalSeparator Method**

The DecimalFormat class also provides a setDecimalSeparator() method that can be used to set the decimal separator. The following code shows how to use it:

```
DecimalFormat format = new DecimalFormat("#.##");
format.setDecimalSeparator('.');
```

**Section 4: Conclusion**

In this tutorial, we learned how to change the decimal separator of DecimalFormat from comma to dot/point in Java. We saw two different ways to do this - using the DecimalFormatSymbols class and the setDecimalSeparator() method.
