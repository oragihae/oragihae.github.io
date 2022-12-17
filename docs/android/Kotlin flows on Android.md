---
layout: default
title: Kotlin flows on Android
parent: Android
---

# Kotlin flows on Android

- [docs](https://developer.android.com/kotlin/flow)

- 코루틴에서 Flow는 단일 값만 반환하는 정지 함수와 달리 여러 값을 순차적으로 내보낼 수 있는 유형
- 예를 들면 Flow를 사용하여 데이터베이스에서 실시간 업데이트를 수신 할 수 있음

- Flow은 코루틴을 기반으로 빌드되며 여러 값을 제공할 수 있음
- Flow은 비동기식으로 계산할 수 있는 데이터 스트림의 개념
- 내보낸 값은 동일한 유형이어야 함
- 예를 들어 Flow<Int>는 정수 값을 내보내는 Flow

- Flow은 값 시퀀스를 생성하는 Iterator와 매우 비슷하지만 정지 함수를 사용하여 값을 비동기적으로 생성하고 사용함
- 예를 들어 Flow는 기본 스레드를 차단하지 않고 다음 값을 생성할 네트워크 요청을 안전하게 만들 수 있음

데이터 스트림에는 다음과 같은 3가지 항목이 있음

![](../../assets/images/Kotlin flows on Android 00.png)

- 생산자
  - 스트림에 추가되는 데이터를 생산
  - 코루틴 덕분에 Flow에서 비동기적으로 데이터가 생산될 수 있음
- (선택사항) 중개자
  - 스트림에 내보내는 각각의 값이나 스트림 자체를 수정할 수 있음
- 소비자
  - 스트림의 값을 사용


안드로이드에서 저장소는 일반적으로 UI 데이터 생산자임, 이때 사용자 인터페이스 (UI)는 최종적으로 데이터를 표시하는 소비자

UI 레이어가 사용자 입력 이벤트의 생산자이고 계층 구조의 다른 레이어가 이 이벤트를 사용하기도 함

생산자와 소비자 사이의 레이어는 일반적으로 다음 레이어의 요구사항에 맞게 조정하기 위해 데이터 스트림을 수정하는 중개자 역할을 함


## Flow 만들기


```kotlin
class NewsRemoteDataSource(
    private val newsApi: NewsApi,
    private val refreshIntervalMs: Long = 5000
) {
    val latestNews: Flow<List<ArticleHeadline>> = flow {
        while(true) {
            val latestNews = newsApi.fetchLatestNews()
            emit(latestNews) // Emits the result of the request to the flow
            delay(refreshIntervalMs) // Suspends the coroutine for some time
        }
    }
}

// Interface that provides a way to make network requests with suspend functions
interface NewsApi {
    suspend fun fetchLatestNews(): List<ArticleHeadline>
}
```


