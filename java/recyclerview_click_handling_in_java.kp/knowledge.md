---
title: Handle clicks in a recyclerview
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Set an OnClickListener on the RecyclerView and override the onClick method to perform the desired action.
---

**Contents**

[TOC]

1. Implement an OnClickListener 

```java
public class MyRecyclerViewAdapter extends RecyclerView.Adapter<MyRecyclerViewAdapter.ViewHolder> {

  private OnItemClickListener mListener;

  public interface OnItemClickListener {
    void onItemClick(int position);
  }

  public void setOnItemClickListener(OnItemClickListener listener) {
    mListener = listener;
  }

  // ...

}
```

2. Attach the OnClickListener to the ViewHolder 

```java
public class ViewHolder extends RecyclerView.ViewHolder {

  public ViewHolder(@NonNull View itemView, final OnItemClickListener listener) {
    super(itemView);

    itemView.setOnClickListener(new View.OnClickListener() {
      @Override
      public void onClick(View v) {
        if (listener != null) {
          int position = getAdapterPosition();
          if (position != RecyclerView.NO_POSITION) {
            listener.onItemClick(position);
          }
        }
      }
    });
  }

}
```

3. Set the OnClickListener to the RecyclerView 

```java
MyRecyclerViewAdapter adapter = new MyRecyclerViewAdapter();
adapter.setOnItemClickListener(new MyRecyclerViewAdapter.OnItemClickListener() {
  @Override
  public void onItemClick(int position) {
    // do something
  }
});
recyclerView.setAdapter(adapter);
```

4. Handle the OnClick Event 

```java
@Override
public void onItemClick(int position) {
  // do something
}
```
