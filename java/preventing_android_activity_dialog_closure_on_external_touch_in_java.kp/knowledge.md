---
title: Stop Android activity dialog from closing when touched outside
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Set the activity`s window flag to FLAG\_NOT\_TOUCH\_MODAL.
---

**Contents**

[TOC]

1. **Override onTouchEvent Method**

By overriding the onTouchEvent method of the Activity, you can detect if the user has touched outside the dialog window. If so, you can return false to prevent the dialog from closing.

```java
@Override
public boolean onTouchEvent(MotionEvent event) {
    if (event.getAction() == MotionEvent.ACTION_OUTSIDE) {
        return false;
    }
    return true;
}
```

2. **Disable Dismiss on Touch Outside**

If you are using an AlertDialog, you can set the cancelable property to false to prevent the dialog from closing when the user touches outside the window.

```java
AlertDialog dialog = new AlertDialog.Builder(context)
    .setCancelable(false)
    .create();
```

3. **Set Window Flags**

You can also set the window flags to prevent the dialog from closing when the user touches outside the window.

```java
dialog.getWindow().setFlags(WindowManager.LayoutParams.FLAG_NOT_TOUCH_MODAL,
                            WindowManager.LayoutParams.FLAG_NOT_TOUCH_MODAL);
```

4. **Set OnCancelListener**

You can also set an OnCancelListener to your dialog to detect when the user is trying to cancel the dialog. When the user tries to cancel the dialog, you can return false to prevent the dialog from closing.

```java
dialog.setOnCancelListener(new DialogInterface.OnCancelListener() {
    @Override
    public void onCancel(DialogInterface dialog) {
        return false;
    }
});
```
