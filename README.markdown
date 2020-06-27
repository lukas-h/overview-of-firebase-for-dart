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

### Types of packages
- `interop library`: direct library to access firebase products for specific platforms
- `native library`: direct library to access firebase products for *all platforms, Dart can run on*
- `wrapper`: approach to create a more abstract API to access firebase products for multiple platforms by bundling 'direct libraries'
- `ORM` (object relational mapping): libraries that help you serialize and deserialize the data between the database and your data models
- `helper`: tools that help you work with firebase in any way

# Packages

### [FirebaseExtended/flutterfire](https://github.com/FirebaseExtended/flutterfire) `interop library`

> Firebase plugins for Flutter apps

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|[cloud_firestore](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
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

---

### [FirebaseExtended/firebase-dart](https://github.com/FirebaseExtended/firebase-dart) `interop library`

> Dart wrapper for Firebase

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
| cloud_firestore| | | | | |:white_check_mark:|
|cloud_functions (https call api)| | | | | |:white_check_mark:|
|firebase_analytics| | | | | |:white_check_mark:|
|firebase_auth| | | | | |:white_check_mark:|
|firebase_core| | | | | |:white_check_mark:|
|firebase_database| | | | |:white_check_mark:|:white_check_mark:|
|firebase_messaging| | | | | |:white_check_mark:|
|firebase_performance| | | | | |:white_check_mark:|
|firebase_remote_config| | | | | |:white_check_mark:|
|firebase_storage| | | | | |:white_check_mark:|

---

### [cachapa/firedart](https://github.com/cachapa/firedart) `native library`

> A dart-native implementation of the Firebase Auth and Firestore SDKs

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|cloud_firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|firebase_auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [abdulaziz-mohammed/firestore_entity](https://github.com/abdulaziz-mohammed/firestore_entity) `ORM`

> A Firestore Wrapper library for binding and mapping documents to dart classes. Enjoy !

It is an extension to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

platform support is given due to the dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [fluttercommunity/firebase_dart_sdk](https://github.com/fluttercommunity/firebase_dart_sdk) `native library`

> Unofficial Firebase Flutter SDK. Maintainer: @long1eu

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|[firebase_auth](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|[firebase_storage](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|[firebase_firestore](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [atn832/cloud_firestore_mocks](https://github.com/atn832/cloud_firestore_mocks) `helper`

> Fakes to write unit tests for Cloud Firestore. Instantiate a MockFirestoreInstance, then pass it around your project as if it were a FirestoreInstance. This fake acts like Firestore except it will only keep the state in memory. To help debug, you can use MockFirestoreInstance.dump() to see what's in the fake database. This is useful to set up the state of your database, then check that your UI behaves the way you expect.

platform support is given due to the dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---
