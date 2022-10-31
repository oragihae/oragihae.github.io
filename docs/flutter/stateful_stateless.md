---
layout: default
title: Stateful vs Stateless Widgets
parent: Flutter
nav_order: 4
---

# Stateful vs Stateless Widgets

- [Stateful and stateless widgets](https://docs.flutter.dev/development/ui/interactive#stateful-and-stateless-widgets)

## StatefulWidget

- 위젯이 변경 가능한 경우 (예를 들면 user interacts)
- Checkbox, Radio, Slider, InkWell, Form, TextField가 stateful 위젯의 예

- 위젯의 state는 State 객체에 저장됨
- 위젯의 state와 위젯의 appearance로 각각 분리
- 위젯의 state가 바뀌면 State 객체는 setState()를 호출하여 프레임워크가 다시 위젯을 그리도록 지시함


## StatelessWidget

- stateless 위젯은 절대 바뀌지 않음
- Icon, IconButton, Text가 stateless 위젯의 예

