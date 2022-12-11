---
layout: default
title: registerForActivityResult
parent: Android
---

# registerForActivityResult

- [Getting a result from an activity](https://developer.android.com/training/basics/intents/result)

원래 startActivityForResult(), onActivityResult() APIs 사용하던거를 
AndroidX Activity, Fragment 부터 도입된 Activity Result APIs를 사용하는 것이 좋음


```kotlin
val getContent = registerForActivityResult(GetContent()) { uri: Uri? ->
    // Handle the returned Uri
}
```