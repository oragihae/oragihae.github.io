---
layout: default
title: XML
parent: Flutter
nav_order: 2
---

# XML 파싱

- [pub.dev: xml](https://pub.dev/packages/xml)

## XmlDocument.parse

```dart
final bookshelfXml = '''<?xml version="1.0"?>
    <bookshelf>
      <book>
        <title lang="en">Growing a Language</title>
        <price>29.99</price>
      </book>
      <book>
        <title lang="en">Learning XML</title>
        <price>39.95</price>
      </book>
      <price>132.00</price>
    </bookshelf>''';
final document = XmlDocument.parse(bookshelfXml);
```

일단 XmlDocument.parse로 파싱

## findAllElements

```dart
final titles = document.findAllElements('title');
```

title의 elements를 전체에서 다 뽑아냄

```dart
titles
    .map((node) => node.text);
```

이런식으로 각 element 사용 가능
위와 같은 경우 Iterable 임

```dart
titles
    .map((node) => node.text)
    .toList();
```

list로 받고 싶으면 toList() 하면 됨
