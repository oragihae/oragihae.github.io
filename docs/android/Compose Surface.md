---
layout: default
title: Compose Surface
parent: Android
---

# Compose Surface

- [docs](https://developer.android.com/reference/kotlin/androidx/compose/material/package-summary#Surface(androidx.compose.ui.Modifier,androidx.compose.ui.graphics.Shape,androidx.compose.ui.graphics.Color,androidx.compose.ui.graphics.Color,androidx.compose.foundation.BorderStroke,androidx.compose.ui.unit.Dp,kotlin.Function0))

- [When should I use Android Jetpack Compose Surface composable?](https://stackoverflow.com/questions/65918835/when-should-i-use-android-jetpack-compose-surface-composable)

```kotlin
Surface(
    color = MaterialTheme.colors.primarySurface,
    border = BorderStroke(1.dp, MaterialTheme.colors.secondary),
    shape = RoundedCornerShape(8.dp),
    elevation = 8.dp
) {
    Text(
        text = "example",
        modifier = Modifier.padding(8.dp)
    )
}

```

```kotlin
val shape = RoundedCornerShape(8.dp)
val shadowElevationPx = with(LocalDensity.current) { 2.dp.toPx() }
val backgroundColor = MaterialTheme.colors.primarySurface

Text(
    text = "example",
    color = contentColorFor(backgroundColor),
    modifier = Modifier
        .graphicsLayer(shape = shape, shadowElevation = shadowElevationPx)
        .background(backgroundColor, shape)
        .border(1.dp, MaterialTheme.colors.secondary, shape)
        .padding(8.dp)
)
```

두 코드 다 동일한 결과를 가져오지만 코드상 Surface로 구현하는 것이 나음