---
title: What is the process for incorporating a jtable into a jpanel with a null layout?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Add the JTable to the JPanel using the JPanel`s add() method.
---

**Contents**

[TOC]

## Section 1: Create the JTable

1. Create a `JTable` object and pass in the column names and the row data.

```java
String[] columnNames = {"ID", "Name", "Age"};
Object[][] rowData = {
    {1, "John", 25},
    {2, "Mary", 30},
    {3, "Bob", 28}
};

JTable table = new JTable(rowData, columnNames);
```

## Section 2: Add the JTable to the JPanel

1. Create a `JPanel` with `null` layout.

```java
JPanel panel = new JPanel(null);
```

2. Set the bounds of the `JTable` to the desired size and position.

```java
table.setBounds(x, y, width, height);
```

3. Add the `JTable` to the `JPanel`.

```java
panel.add(table);
```

## Section 3: Configure the JTable

1. Set the preferred size of the `JTable` to match the bounds.

```java
table.setPreferredSize(new Dimension(width, height));
```

2. Set the selection mode of the `JTable` to allow multiple selections.

```java
table.setSelectionMode(ListSelectionModel.MULTIPLE_INTERVAL_SELECTION);
```

## Section 4: Finalize the JTable

1. Set the `JTable` to be visible.

```java
table.setVisible(true);
```

2. Add the `JPanel` to the parent container.

```java
parentContainer.add(panel);
```
