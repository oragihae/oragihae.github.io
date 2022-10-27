---
layout: default
title: Http
nav_order: 1
---

# Flutter 에서 Http 통신

- [pub.dev: http](https://pub.dev/packages/http)

http 패키지 사용

## 1. dependencies 추가

dependencies는 pubspec.yaml 안에서 정의 가능

```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^0.13.5
```

## 2. Pub get

Pub get 클릭해서 패키지 가져오기

## 3. 패키지 import

```dart

import 'package:http/http.dart' as http;

```

## 4. url 접속


```dart

class _MyHomePageState extends State<MyHomePage> {
  String result = '';

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Text(result),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () async {
          var url = 'http://www.google.com';
          var response = await http.get(Uri.parse(url));
          setState(() {
            result = response.body;
          });
        },
        child: const Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
}

```

테스트로 구글로 접속
