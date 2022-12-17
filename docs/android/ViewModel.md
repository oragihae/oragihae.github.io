---
layout: default
title: ViewModel
parent: Android
nav_order: 2
---

# ViewModel

- [docs: ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel)

## 주의 
ViewModel은 a view, Lifecycle, or any class that may hold a reference to the activity context를 참조하면 안됨

ViewModel 라이프 사이클이 UI 보다 크기 때문, 가지고 있으면 메모리 누수의 원인이 됨

