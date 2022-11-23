---
layout: default
title: RecyclerView
parent: Android
nav_order: 6
has_children: true
---

# RecyclerView

- [docs: Create dynamic lists with RecyclerView](https://developer.android.com/develop/ui/views/layout/recyclerview)
- [코틀린 샘플](https://github.com/android/views-widgets-samples/tree/main/RecyclerViewKotlin/)

## 코틀린 샘플

![](../../assets/images/Android RecyclerView Sample (Kotlin).png)

샘플 보면 꽃 이미지랑 꽃 이름이 RecyclerView로 구현이 되어 있음

### FlowersAdapter

```kotlin
class FlowersAdapter(private val onClick: (Flower) -> Unit) :
    ListAdapter<Flower, FlowersAdapter.FlowerViewHolder>(FlowerDiffCallback) {
```

- onClick
- FlowerDiffCallback

