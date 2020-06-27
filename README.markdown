# State of Firebase for Dart :fire::dart:
## A list of all libraries that (try to) cover Firebase for Dart

### *Why?*
Dart is lacking an official implementation of a firebase sdk in native Dart code.

The existing, wrappers ([flutterfire](https://github.com/FirebaseExtended/flutterfire), [firebase-dart](https://github.com/FirebaseExtended/firebase-dart)) around the official JS, iOS and Android SDKs are inside the [*FirebaseExtended*](https://github.com/FirebaseExtended) organisation on Github, which means: 
["Projects that are not officially staffed by Googlers ..."](https://github.com/FirebaseExtended).

If you want to use Firebase on *different target platforms* (Flutter, Dart for Web or VM) you have *different packages*, varying syntax or even lacking support of many Firebase features.

Besides these packages there are also ...
- unofficial attempts to create unified wrappers for all target platforms
- unofficial and incomplete attempts to create a Dart native package for Firebase 

### This document is supposed to give an overview of Dart packages for Firebase.

- If you'd like to contribute or help me improve this list, please open pull requests or issues.
- If you want to discuss, please open issues. 

### Types of packages
- `interop library`: library to access firebase products for specific platforms, based on an interface to another programming language
- `native library`: direct library to access firebase products, written in Dart, therefore for *all platforms, Dart can run on*
- `wrapper`: approach to create a more abstract API to access firebase products for multiple platforms by bundling 'direct libraries'
- `ORM` (object relational mapping): libraries that help you serialize and deserialize the data between the database and your data models
- `helper`: tools that help you work with firebase in any way

# Packages

### [FirebaseExtended/flutterfire](https://github.com/FirebaseExtended/flutterfire) `interop library`

> Firebase plugins for Flutter apps

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|[Firestore](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
|[Functions](https://pub.dev/packages/cloud_functions) (https call api)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
|[Admob](https://pub.dartlang.org/packages/firebase_admob)|:white_check_mark:|:white_check_mark:||   |   |   |
|[Analytics](https://pub.dartlang.org/packages/firebase_analytics)|:white_check_mark:|:white_check_mark:||   |   |   |
|[Auth](https://pub.dartlang.org/packages/firebase_analytics)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|   |
|[Core](https://pub.dartlang.org/packages/firebase_core)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|   |
|[Crashlytics](https://pub.dartlang.org/packages/firebase_crashlytics)|:white_check_mark:|:white_check_mark:|   |:white_check_mark:(macOs)|   |
|[Realtime Database](https://pub.dartlang.org/packages/firebase_database)|:white_check_mark:|:white_check_mark:||   |   |   |
|[Dynamic Links](https://pub.dartlang.org/packages/firebase_dynamic_links)|:white_check_mark:|:white_check_mark:||   |   |   |
|[In App Messaging](https://pub.dartlang.org/packages/firebase_in_app_messaging)|:white_check_mark:|:white_check_mark:||   |   |   |
|[Messaging](https://pub.dartlang.org/packages/firebase_messaging)|:white_check_mark:|:white_check_mark:||   |   |   |
|[ML Vision](https://pub.dartlang.org/packages/firebase_ml_vision)|:white_check_mark:|:white_check_mark:||   |   |   |
|[Performance](https://pub.dartlang.org/packages/firebase_performance)|:white_check_mark:|:white_check_mark:||   |   |   |
|[Remote Config](https://pub.dartlang.org/packages/firebase_remote_config)|:white_check_mark:|:white_check_mark:|   |   |   |
|[Storage](https://pub.dartlang.org/packages/firebase_storage)|:white_check_mark:|:white_check_mark:||:white_check_mark:(macOs)|   |   |

---

### [FirebaseExtended/firebase-dart](https://github.com/FirebaseExtended/firebase-dart) `interop library`

> Dart wrapper for Firebase

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore| | | | | |:white_check_mark:|
|Functions (https call api)| | | | | |:white_check_mark:|
|Analytics| | | | | |:white_check_mark:|
|Auth| | | | | |:white_check_mark:|
|Core| | | | | |:white_check_mark:|
|Realtime Database| | | | |:white_check_mark:|:white_check_mark:|
|Messaging| | | | | |:white_check_mark:|
|Performance| | | | | |:white_check_mark:|
|Remote Config| | | | | |:white_check_mark:|
|Storage| | | | | |:white_check_mark:|

---

### [cachapa/firedart](https://github.com/cachapa/firedart) `native library`

> A dart-native implementation of the Firebase Auth and Firestore SDKs

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

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
|Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Storage|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Core|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [atn832/cloud_firestore_mocks](https://github.com/atn832/cloud_firestore_mocks) `helper`

> Fakes to write unit tests for Cloud Firestore. Instantiate a MockFirestoreInstance, then pass it around your project as if it were a FirestoreInstance. This fake acts like Firestore except it will only keep the state in memory. To help debug, you can use MockFirestoreInstance.dump() to see what's in the fake database. This is useful to set up the state of your database, then check that your UI behaves the way you expect.

platform support is given due to the dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [fluttercommunity/firestore_helpers](https://github.com/fluttercommunity/firestore_helpers) `helper`

> Firestore Helpers - Firestore helper function to create dynamic and location based queries.

platform support is given due to the dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [pulyaevskiy/firebase-functions-interop](https://github.com/pulyaevskiy/firebase-functions-interop) `interop library`  

> Write Firebase Cloud functions in Dart, run in Node.js. This is an early development preview, open-source project.

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|cloud functions|
|---|---|---|---|---|---|---|---|
|firebase-functions-interop|||||||:white_check_mark:|

features:
- [x] functions
- [x] functions.config
- [ ] functions.analytics
- [x] functions.auth
- [x] functions.firestore :fire:
- [x] functions.database
- [x] functions.https
- [x] functions.pubsub
- [x] functions.storage
- [ ] functions.remoteConfig

--- 

### [apptreesoftware/crossfire](https://github.com/apptreesoftware/crossfire) `wrapper` [Discontinued] 

> Cross-platform APIs for Firebase.  
>- crossfire - platform-agnostic firebase API  
>- crossfire_flutter - flutter implementation  
>- crossfire_web - web implementation  

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)||:white_check_mark:|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)||:white_check_mark:|

---

### [mono0926/flutter_firestore_ref](https://github.com/mono0926/flutter_firestore_ref) `wrapper`  

> Cross-platform(including web) Firestore type-safe wrapper.

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||

