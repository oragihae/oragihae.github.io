---
layout: default
title: WindowInfoTracker
parent: Android
---

# WindowInfoTracker

- [docs](https://developer.android.com/reference/kotlin/androidx/window/layout/WindowInfoTracker?hl=ko)

```kotlin
fun windowLayoutInfo(activity: Activity): Flow<WindowLayoutInfo>
```

- A Flow of WindowLayoutInfo that contains all the available features.
- A WindowLayoutInfo contains a List of DisplayFeature that intersect the associated android.view.Window.

- The first WindowLayoutInfo will not be emitted until Activity.onStart has been called. 
- which values you receive and when is device dependent. 
- It is recommended to test scenarios where there is a long delay between subscribing and receiving the first value or never receiving a value, since it may differ between hardware implementations.

- Since the information is associated to the Activity you should not retain the Flow across Activity recreations. 
- Doing so can result in unpredictable behavior such as a memory leak or incorrect values for WindowLayoutInfo.
