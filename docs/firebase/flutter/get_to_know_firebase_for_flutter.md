---
layout: default
title: Get to know Firebase for Flutter
parent: Flutter
grand_parent: Firebase
---

# Get to know Firebase for Flutter

- [docs: Get to know Firebase for Flutter](https://firebase.google.com/codelabs/firebase-get-to-know-flutter#0)
- [예제 코드: firebase-get-to-know-flutter/step_02](https://github.com/flutter/codelabs/tree/main/firebase-get-to-know-flutter/step_02/lib)

## step_02

main.dart 가 있고 scr 폴더 안에 authentication.dart, widgets.dart 2개 파일이 있음

``dart
class ApplicationState extends ChangeNotifier {
  ApplicationState() {
    init();
  }

  bool _loggedIn = false;
  bool get loggedIn => _loggedIn;

  Future<void> init() async {
    await Firebase.initializeApp(
        options: DefaultFirebaseOptions.currentPlatform);

    FirebaseUIAuth.configureProviders([
      EmailAuthProvider(),
    ]);

    FirebaseAuth.instance.userChanges().listen((user) {
      if (user != null) {
        _loggedIn = true;
      } else {
        _loggedIn = false;
      }
      notifyListeners();
    });
  }
}
``