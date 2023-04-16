---
title: Programmatically adjust the margins of a linearlayout
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: LinearLayout.LayoutParams can be used to set margins programmatically in a LinearLayout.
---

**Contents**

[TOC]

#### Setting Margins

To set margins in a LinearLayout programmatically in Java, use the setMargins() method. This method takes four parameters: the left, top, right, and bottom margins.

```
LinearLayout.LayoutParams params = new LinearLayout.LayoutParams(
    LinearLayout.LayoutParams.WRAP_CONTENT,
    LinearLayout.LayoutParams.WRAP_CONTENT
);
params.setMargins(left, top, right, bottom);
```

#### Setting Margin in Density-Independent Pixels

In addition to setting margins in pixels, you can also set them in density-independent pixels (dp). To do this, use the setMarginStart() and setMarginEnd() methods. These methods take two parameters: the start and end margins.

```
LinearLayout.LayoutParams params = new LinearLayout.LayoutParams(
    LinearLayout.LayoutParams.WRAP_CONTENT,
    LinearLayout.LayoutParams.WRAP_CONTENT
);
params.setMarginStart(start);
params.setMarginEnd(end);
```

#### Setting Margin in RelativeLayout

If you are using a RelativeLayout instead of a LinearLayout, you can use the setMarginStart() and setMarginEnd() methods to set the left and right margins. This will set the margins in density-independent pixels.

```
RelativeLayout.LayoutParams params = new RelativeLayout.LayoutParams(
    RelativeLayout.LayoutParams.WRAP_CONTENT,
    RelativeLayout.LayoutParams.WRAP_CONTENT
);
params.setMarginStart(start);
params.setMarginEnd(end);
```

#### Setting Margin in ConstraintLayout

If you are using a ConstraintLayout instead of a LinearLayout, you can use the setMarginStart() and setMarginEnd() methods to set the left and right margins. This will set the margins in density-independent pixels.

```
ConstraintLayout.LayoutParams params = new ConstraintLayout.LayoutParams(
    ConstraintLayout.LayoutParams.WRAP_CONTENT,
    ConstraintLayout.LayoutParams.WRAP_CONTENT
);
params.setMarginStart(start);
params.setMarginEnd(end);
```
