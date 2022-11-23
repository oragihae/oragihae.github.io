---
layout: default
title: LayoutInflater
parent: Android
nav_order: 7
---

# LayoutInflater

- [docs: LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater)

레이아웃 XML 파일을 android.view.View 객체로 인스턴스화 하는데 쓰임

## inflate

inflate 메소드가 여러 개 인데 그 중 하나 가져옴

```python
open fun inflate(
    resource: Int, 
    root: ViewGroup?, 
    attachToRoot: Boolean
): View!
```

- [docs: inflate](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#inflate_2)

### root
Optional view to be the parent of the generated hierarchy (if attachToRoot is true),

or else simply an object that provides a set of LayoutParams values for root of the returned hierarchy (if attachToRoot is false.) 

This value may be null.

### attachToRoot
Whether the inflated hierarchy should be attached to the root parameter? 

If false, root is only used to create the correct subclass of LayoutParams for the root view in the XML.
