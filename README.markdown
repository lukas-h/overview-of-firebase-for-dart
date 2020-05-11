# State of Firebase for Dart :fire::dart:
## A list of all libraries that (try to) cover Firebase for Dart

### *Why?*
Dart is lacking an official implementation of a firebase sdk in native Dart code.

The existing, wrappers ([flutterfire](https://github.com/FirebaseExtended/flutterfire), [firebase-dart](https://github.com/FirebaseExtended/firebase-dart)) around the official JS, iOS and Android SDKs are on the [*FirebaseExtended*](https://github.com/FirebaseExtended) organisation on Github, which means: 
["Projects that are not officially staffed by Googlers ..."](https://github.com/FirebaseExtended).

If you want to use Firebase on different target platforms (Flutter, Dart for Web or VM) you have different packages, varying syntax or even lacking support of many Firebase features.

Besides these packages there are also ...
- unofficial attempts to create unified wrappers for all target platforms
- unofficial and incomplete attempts to create a Dart native package for Firebase 

### This document is supposed to give an overview of packages for Firebase.
- If you'd like to contribute or help me improve this list, please open pull requests or issues.
- If you want to discuss, please open issues. 

# Packages

### [FirebaseExtended/flutterfire](https://github.com/FirebaseExtended/flutterfire)
|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
| [cloud_firestore](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
|[cloud_functions](https://pub.dev/packages/cloud_functions) (https call api)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
|[firebase_admob](https://pub.dartlang.org/packages/firebase_admob)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_analytics](https://pub.dartlang.org/packages/firebase_analytics)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_auth](https://pub.dartlang.org/packages/firebase_analytics)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|   |
|[firebase_core](https://pub.dartlang.org/packages/firebase_core)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|   |
|[firebase_crashlytics](https://pub.dartlang.org/packages/firebase_crashlytics)|:white_check_mark:|:white_check_mark:|   |:white_check_mark:(macOs)|   |
|[firebase_database](https://pub.dartlang.org/packages/firebase_database)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_dynamic_links](https://pub.dartlang.org/packages/firebase_dynamic_links)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_in_app_messaging](https://pub.dartlang.org/packages/firebase_in_app_messaging)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_messaging](https://pub.dartlang.org/packages/firebase_messaging)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_ml_vision](https://pub.dartlang.org/packages/firebase_ml_vision)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_performance](https://pub.dartlang.org/packages/firebase_performance)|:white_check_mark:|:white_check_mark:||   |   |   |
|[firebase_remote_config](https://pub.dartlang.org/packages/firebase_remote_config)|:white_check_mark:|:white_check_mark:|   |   |   |
|[firebase_storage](https://pub.dartlang.org/packages/firebase_storage)|:white_check_mark:|:white_check_mark:||:white_check_mark:(macOs)|   |   |
