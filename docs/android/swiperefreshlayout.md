---
layout: default
title: SwipeRefreshLayout
parent: Android
---

# SwipeRefreshLayout

- [Adding Swipe-to-Refresh To Your App](https://developer.android.com/develop/ui/views/touch-and-input/swipe/add-swipe-interface)

```xml
<androidx.swiperefreshlayout.widget.SwipeRefreshLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/swiperefresh"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ListView
        android:id="@android:id/list"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</androidx.swiperefreshlayout.widget.SwipeRefreshLayout>
```

- SwipeRefreshLayout은 ListView 나 GridView 만 지원
- "@android:id/list" 라고 설정하면 갱신됨
