---
layout: default
title: Scaffold
parent: Flutter
nav_order: 5
---

# Scaffold

- [docs: Scaffold class](https://api.flutter.dev/flutter/material/Scaffold-class.html)

- 기본적인 Material Design을 시각적인 레이아웃 구조로 implements

```dart
class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  int _count = 0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Sample Code'),
      ),
      body: Center(
        child: Text('You have pressed the button $_count times.'),
      ),
      bottomNavigationBar: BottomAppBar(
        shape: const CircularNotchedRectangle(),
        child: Container(height: 50.0),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () => setState(() {
          _count++;
        }),
        tooltip: 'Increment Counter',
        child: const Icon(Icons.add),
      ),
      floatingActionButtonLocation: FloatingActionButtonLocation.centerDocked,
    );
  }
}
```

- 예를 들면 위 코드에서는 appBar, body, bottomNavigationBar, floatingActionButton, floatingActionButtonLocation 를 implements
- 어떤 Properties가 있는지는 문서에 나와있음
