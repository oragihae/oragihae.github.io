---
layout: default
title: 명명규칙
parent: Python
nav_order: 2
---

# 명명규칙

- [docs: 명명규칙](https://peps.python.org/pep-0008/#naming-conventions)



## 패키지, 모듈 이름

```python
lowercase
```

## 클래스 이름

```python
CapitalizedWords
```

## 타입 변수 이름

```python
CapitalizedWords
```

- 단, 짧은 CapitalizedWords
- 예를 들면 T, AnyStr, Num

## Exception 이름

- exceptions는 클래스이기 때문에 클래스 명명법을 따름
- 다만, error일 경우 앞에 Error을 붙여야 함 (접미사)

## 전역 변수 이름

```python
lowercase

lower_case_with_underscores
```

- 한 모듈 내에서만 사용 할 것
- 함수랑 명명법 같음

## 함수 및 변수 이름

```python
lowercase

lower_case_with_underscores
```

- 가독성을 높이기 위해 _ 사용 가능

## 함수 및 Method Argument

- 항상 self를 인스턴스 메소드의 첫번째 argument로 사용 할 것
- 항상 cls를 클래스 메소드의 첫번째 argument로 사용 할 것

## 메소드 이름 및 인스턴스 변수

```python
lowercase

lower_case_with_underscores
```

- 함수의 명명규칙 사용

## 상수

```python
MAX_OVERFLOW

TOTAL
```

> 일단 여기까지
> 뒤에 내용 좀 있음
