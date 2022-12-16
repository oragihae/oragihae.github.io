---
layout: default
title: ComponentActivity vs. AppCompatActivity
parent: Android
---

# ComponentActivity vs. AppCompatActivity

- [ComponentActivity vs AppCompactActivity in Android Jetpack Compose](https://stackoverflow.com/questions/67891362/componentactivity-vs-appcompactactivity-in-android-jetpack-compose)

AppCompatActivity extends FragmentActivity which extends ComponentActivity.

ComponentActivity has all you need for a Compose-only app.
If you need AppCompat APIs, an AndroidView which works with AppCompat or MaterialComponents theme, or you need Fragments then use AppCompatActivity.

Note: it requires at least the AppCompat 1.3.0 version.