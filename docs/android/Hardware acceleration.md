---
layout: default
title: Hardware acceleration
parent: Android
---

# Hardware acceleration

- [Hardware acceleration](https://developer.android.com/topic/performance/hardware-accel)

## 왜 쓰나...

- 안드로이드 3.0 (API 레벨은 11) 부터 안드로이드 2D 렌더링 파이프라인은 하드웨어 가속화를 지원함
- 이 뜻은 View의 canvas 위에 수행되는 모든 드로잉 작업을 GPU로 작업하겠다는 거임
- 하드웨어 가속을 활성화하는데 필요한 리소스가 증가하기 떄문에 앱은 좀 더 많은 RAM을 사용함


- 하드웨어 가속화는 타겟 API 레벨이 14 이상이면 기본적으로 활성화 됨
- 물론 명시적으로 비활성화 할 수도 있음
- 만약 application이 표준 view와 Drawables 만 사용한다면 turning it on globally should not cause any adverse drawing effects. 
- 하지만 하드웨어 가속화는 모든 2D 드로잉 작업을 서포팅하지 않으므로 커스텀한 뷰나 드로잉 호출에 영향을 줄 수 있음
- Problems usually manifest themselves as invisible elements, exceptions, or wrongly rendered pixels. 
- To remedy this, Android gives you the option to enable or disable hardware acceleration at multiple levels.
- [Control hardware acceleration](https://developer.android.com/topic/performance/hardware-accel#controlling) 참고


- If your application performs custom drawing, test your application on actual hardware devices with hardware acceleration turned on to find any problems. 
- The Support for drawing operations section describes known issues with hardware acceleration and how to work around them.

- OpenGL with the Framework APIs and Renderscript 도 참고


## 하드웨어 가속 활성화

```
<application android:hardwareAccelerated="true" ...>
```
