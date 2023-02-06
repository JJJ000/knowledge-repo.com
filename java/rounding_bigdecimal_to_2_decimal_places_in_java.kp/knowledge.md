---
title: Always ensure bigdecimal values are rounded to two decimal places
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the BigDecimal.setScale(2, RoundingMode.HALF\_UP) method to round a BigDecimal to always have two decimal places.
---

**Contents**

[TOC]

### Using setScale

BigDecimal has a setScale method that takes two parameters - the number of decimal places to round to, and a rounding mode. This method modifies the existing BigDecimal object and returns a new BigDecimal object.

For example, to round a BigDecimal to two decimal places, you can use the following code:

```
BigDecimal bd = new BigDecimal("123.4567");
BigDecimal rounded = bd.setScale(2, RoundingMode.HALF_UP);
System.out.println(rounded); // 123.46
```

### Using format

You can also use the format method of the DecimalFormat class to round BigDecimal to two decimal places. This method takes a BigDecimal object as a parameter and returns a formatted String.

For example, to round a BigDecimal to two decimal places, you can use the following code:

```
BigDecimal bd = new BigDecimal("123.4567");
DecimalFormat df = new DecimalFormat("#.00");
String formatted = df.format(bd);
System.out.println(formatted); // 123.46
```

### Using MathContext

The MathContext class provides a way to specify the precision and rounding mode for calculations with BigDecimal objects. You can use the MathContext constructor to create a MathContext object with the desired precision and rounding mode.

For example, to round a BigDecimal to two decimal places, you can use the following code:

```
BigDecimal bd = new BigDecimal("123.4567");
MathContext mc = new MathContext(2, RoundingMode.HALF_UP);
BigDecimal rounded = bd.round(mc);
System.out.println(rounded); // 123.46
```

### Using doubleValue

The doubleValue method of the BigDecimal class returns a double value rounded to two decimal places. This method does not modify the existing BigDecimal object.

For example, to round a BigDecimal to two decimal places, you can use the following code:

```
BigDecimal bd = new BigDecimal("123.4567");
double rounded = bd.doubleValue();
System.out.println(rounded); // 123.46
```
