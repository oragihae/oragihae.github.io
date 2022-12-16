---
layout: default
title: Compose UI
parent: Android
---

# Compose UI

## Compose의 ConstraintLayout

- [docs](https://developer.android.com/jetpack/compose/layouts/constraintlayout)

- 복잡할 때 쓰기 좋음

- createRefs() 또는 createRefFor()를 사용하여 ConstraintLayout에서 각 컴포저블의 참조를 만듦
- 제약 조건은 constrainAs() modifier를 사용하여 제공됨
- 이 modifier는 참조를 매개변수로 사용하고 본문 람다에 제약 조건을 지정할 수 있게 함
- 제약 조건은 linkTo() 또는 다른 유용한 메서드를 사용하여 지정됨
- parent는 ConstraintLayout 컴포저블 자체에 대한 제약 조건을 지정하는 데 사용할 수 있는 기존 참조

```koltin
@Composable
fun ConstraintLayoutContent() {
    ConstraintLayout {
        // Create references for the composables to constrain
        val (button, text) = createRefs()

        Button(
            onClick = { /* Do something */ },
            // Assign reference "button" to the Button composable
            // and constrain it to the top of the ConstraintLayout
            modifier = Modifier.constrainAs(button) {
                top.linkTo(parent.top, margin = 16.dp)
            }
        ) {
            Text("Button")
        }

        // Assign reference "text" to the Text composable
        // and constrain it to the bottom of the Button composable
        Text("Text", Modifier.constrainAs(text) {
            top.linkTo(button.bottom, margin = 16.dp)
        })
    }
}

```

## Lists and grids

- [docs](https://developer.android.com/jetpack/compose/lists)

- LazyColumn : 세로 스크롤
- LazyRow : 가로 스크롤

```kotlin
import androidx.compose.foundation.lazy.items

@Composable
fun MessageList(messages: List<Message>) {
    LazyColumn {
        items(messages) { message ->
            MessageRow(message)
        }
    }
}
```


## Scaffold

- [Scaffold](https://developer.android.com/jetpack/compose/layouts/material?hl=ko#scaffold)

### AppBar

```kotlin
Scaffold(
    topBar = {
        TopAppBar { /* Top app bar content */ }
    }
) {
    // Screen content
}
```


