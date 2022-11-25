---
layout: default
title: ListView
parent: Flutter
nav_order: 3
---

# ListView

- [docs: ListView class](https://api.flutter.dev/flutter/widgets/ListView-class.html)
- [docs: ListView](https://docs.flutter.dev/development/ui/layout#listview)

## ListView를 구성하는 4가지 옵션

### 1. 기본 생성자는 children으로 List\<Widget> 을 사용

```dart
ListView(
  padding: const EdgeInsets.all(8),
  children: <Widget>[
    Container(
      height: 50,
      color: Colors.amber[600],
      child: const Center(child: Text('Entry A')),
    ),
    Container(
      height: 50,
      color: Colors.amber[500],
      child: const Center(child: Text('Entry B')),
    ),
    Container(
      height: 50,
      color: Colors.amber[100],
      child: const Center(child: Text('Entry C')),
    ),
  ],
)
```

- children: \<Widget>[ ... ] 으로 List를 받음
- 이런 식의 구현은 하위 children 수가 적어야 함
- 왜냐하면 모든 child를 구성하기 때문 (보이는 거만 구성한다거나 그런게 아니라)

### 2. ListView.builder 생성자는 요청 시에 child를 빌드하는 IndexedWidgetBuilder를 사용

```dart
final List<String> entries = <String>['A', 'B', 'C'];
final List<int> colorCodes = <int>[600, 500, 100];

ListView.builder(
  padding: const EdgeInsets.all(8),
  itemCount: entries.length,
  itemBuilder: (BuildContext context, int index) {
    return Container(
      height: 50,
      color: Colors.amber[colorCodes[index]],
      child: Center(child: Text('Entry ${entries[index]}')),
    );
  }
);
```

- child가 많거나 무한인 ListView에 적절함
- 실제로 보이는 children 만 빌더가 호출되기 때문

실제로는 ListView.builder 를 많이 사용 하는 듯 함

---

나머지 2가지는 필요할 때 정리
