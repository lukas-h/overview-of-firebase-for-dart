# State of Firebase for Dart :fire::dart:
## A list of all libraries that (try to) cover Firebase for Dart

### *Why?*
Dart is lacking an official implementation of a firebase sdk in native Dart code.

The existing, wrapper libs ([flutterfire](#firebaseextendedflutterfire-interop-library), [firebase-dart](#firebaseextendedfirebase-dart-interop-library)) around the official JS, iOS and Android SDKs are inside the [*FirebaseExtended*](https://github.com/FirebaseExtended) organisation on Github, which means: 
["Projects that are not officially staffed by Googlers ..."](https://github.com/FirebaseExtended).

Besides these packages there are also ...
- unofficial attempts to create unified wrappers for all target platforms
- unofficial and incomplete attempts to create a Dart native package for Firebase 

In general: If you want to use Firebase on all the *different Dart target platforms* (Flutter, Dart for Web or VM) you have *different packages*, varying syntax or even lacking support of many Firebase features.

### This document is supposed to give an overview of Dart packages for Firebase.

- If you'd like to contribute or help me improve this list, please open pull requests or issues.
- If you want to discuss, please open issues. 

### Types of packages
- `interop library`: library to access firebase products for specific platforms, based on an interface to another programming language
- `native library`: direct library to access firebase products, written in Dart, therefore for *all platforms, Dart can run on*
- `wrapper`: approach to create a more abstract API to access firebase products for multiple platforms by bundling other libraries
- `ORM` (object relational mapping): libraries that help you serialize and deserialize the data between the database and your data models
- `helper`: tools that help you work with firebase in any way

# Packages

### [FirebaseExtended/flutterfire](https://github.com/FirebaseExtended/flutterfire) `interop library`

> Firebase plugins for Flutter apps

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore [![Pub Package](https://img.shields.io/pub/v/cloud_firestore.svg)](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
|Functions (https call api) [![Pub Package](https://img.shields.io/pub/v/cloud_functions.svg)](https://pub.dev/packages/cloud_functions)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||
|Admob [![Pub Package](https://img.shields.io/pub/v/firebase_admob.svg)](https://pub.dev/packages/firebase_admob)|:white_check_mark:|:white_check_mark:||   |   |   |
|Analytics [![Pub Package](https://img.shields.io/pub/v/firebase_analytics.svg)](https://pub.dev/packages/firebase_analytics)|:white_check_mark:|:white_check_mark:||   |   |   |
|Auth [![Pub Package](https://img.shields.io/pub/v/firebase_auth.svg)](https://pub.dev/packages/firebase_auth)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|   |
|Core [![Pub Package](https://img.shields.io/pub/v/firebase_core.svg)](https://pub.dev/packages/firebase_core)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|   |
|Crashlytics [![Pub Package](https://img.shields.io/pub/v/firebase_crashlytics.svg)](https://pub.dev/packages/firebase_crashlytics)|:white_check_mark:|:white_check_mark:|   |:white_check_mark:(macOs)|   |
|Realtime Database [![Pub Package](https://img.shields.io/pub/v/firebase_database.svg)](https://pub.dev/packages/firebase_database)|:white_check_mark:|:white_check_mark:||   |   |   |
|Dynamic Links [![Pub Package](https://img.shields.io/pub/v/firebase_dynamic_links.svg)](https://pub.dev/packages/firebase_dynamic_links)|:white_check_mark:|:white_check_mark:||   |   |   |
|In App Messaging [![Pub Package](https://img.shields.io/pub/v/firebase_in_app_messaging.svg)](https://pub.dev/packages/firebase_in_app_messaging)|:white_check_mark:|:white_check_mark:||   |   |   |
|Messaging [![Pub Package](https://img.shields.io/pub/v/firebase_messaging.svg)](https://pub.dev/packages/firebase_messaging)|:white_check_mark:|:white_check_mark:||   |   |   |
|ML Vision [![Pub Package](https://img.shields.io/pub/v/firebase_ml_vision.svg)](https://pub.dev/packages/firebase_ml_vision)|:white_check_mark:|:white_check_mark:||   |   |   |
|Performance [![Pub Package](https://img.shields.io/pub/v/firebase_performance.svg)](https://pub.dev/packages/firebase_performance)|:white_check_mark:|:white_check_mark:||   |   |   |
|Remote Config [![Pub Package](https://img.shields.io/pub/v/firebase_remote_config.svg)](https://pub.dev/packages/firebase_remote_config)|:white_check_mark:|:white_check_mark:|   |   |   |
|Storage [![Pub Package](https://img.shields.io/pub/v/firebase_storage.svg)](https://pub.dev/packages/firebase_storage)|:white_check_mark:|:white_check_mark:||:white_check_mark:(macOs)|   |   |

---

### [FirebaseExtended/firebase-dart](https://github.com/FirebaseExtended/firebase-dart) `interop library`

> Dart wrapper for Firebase

[![Pub Package](https://img.shields.io/pub/v/firebase.svg)](https://pub.dev/packages/firebase)

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

[![Pub Package](https://img.shields.io/pub/v/firedart.svg)](https://pub.dev/packages/firedart)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [cachapa/fireutil](https://github.com/cachapa/fireutil) `helper`

> A simple CLI utility to push key-value pairs to Firestore. Useful for scripting, e.g. logging system data using crontab.

platform support is given by its dependency to [capacha/firedart](#cachapafiredart-native-library).

--- 

### [abdulaziz-mohammed/firestore_entity](https://github.com/abdulaziz-mohammed/firestore_entity) `ORM`

> A Firestore Wrapper library for binding and mapping documents to dart classes. Enjoy !

[![Pub Package](https://img.shields.io/pub/v/firestore_entity.svg)](https://pub.dev/packages/firestore_entity)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

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

### [fluttercommunity/firestore_helpers](https://github.com/fluttercommunity/firestore_helpers) `helper`

> Firestore Helpers - Firestore helper function to create dynamic and location based queries.

[![Pub Package](https://img.shields.io/pub/v/firestore_helpers.svg)](https://pub.dev/packages/firestore_helpers)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [atn832/cloud_firestore_mocks](https://github.com/atn832/cloud_firestore_mocks) `helper`

> Fakes to write unit tests for Cloud Firestore. Instantiate a MockFirestoreInstance, then pass it around your project as if it were a FirestoreInstance. This fake acts like Firestore except it will only keep the state in memory. To help debug, you can use MockFirestoreInstance.dump() to see what's in the fake database. This is useful to set up the state of your database, then check that your UI behaves the way you expect.

[![Pub Package](https://img.shields.io/pub/v/cloud_firestore_mocks.svg)](https://pub.dev/packages/cloud_firestore_mocks)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [atn832/firebase_auth_mocks](https://github.com/atn832/firebase_auth_mocks) `helper`

> Mocks for Firebase Auth. Use this package with google_sign_in_mocks to write unit tests involving Firebase Authentication.

[![Pub Package](https://img.shields.io/pub/v/firebase_auth_mocks.svg)](https://pub.dev/packages/firebase_auth_mocks)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [atn832/firebase_storage_mocks](https://github.com/atn832/firebase_storage_mocks) `helper`

> Mocks for Firebase Storage. Use this package to write unit tests involving Firebase Storage.

[![Pub Package](https://img.shields.io/pub/v/firebase_storage_mocks.svg)](https://pub.dev/packages/firebase_storage_mocks)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [pulyaevskiy/firebase-functions-interop](https://github.com/pulyaevskiy/firebase-functions-interop) `interop library`  

> Write Firebase Cloud functions in Dart, run in Node.js. This is an early development preview, open-source project.

[![Pub Package](https://img.shields.io/pub/v/firebase_functions_interop.svg)](https://pub.dev/packages/firebase_functions_interop)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|cloud functions|
|---|---|---|---|---|---|---|---|
|firebase-functions-interop||||||:white_check_mark:(NodeJS)|:white_check_mark:|

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

### [pulyaevskiy/firebase-admin-interop](https://github.com/pulyaevskiy/firebase-admin-interop) `interop library`  

> Write server-side Firebase applications in Dart using Node.js as a runtime.

[![Pub Package](https://img.shields.io/pub/v/firebase_admin_interop.svg)](https://pub.dev/packages/firebase_admin_interop)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|cloud functions|
|---|---|---|---|---|---|---|---|
|firebase-functions-interop||||||:white_check_mark:(NodeJS)||

features:
- [x] admin
- [x] admin.auth
- [x] admin.app
- [x] admin.credential
- [x] admin.database
- [x] admin.firestore
- [x] admin.messaging
- [ ] admin.storage

---

### [apptreesoftware/crossfire](https://github.com/apptreesoftware/crossfire) `wrapper` [Discontinued] 

> Cross-platform APIs for Firebase.  
>- crossfire - platform-agnostic firebase API  
>- crossfire_flutter - flutter implementation  
>- crossfire_web - web implementation  

[![Pub Package](https://img.shields.io/pub/v/crossfire.svg)](https://pub.dev/packages/crossfire)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)||:white_check_mark:|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)||:white_check_mark:|

---

### [mono0926/flutter_firestore_ref](https://github.com/mono0926/flutter_firestore_ref) `wrapper`  

> Cross-platform(including web) Firestore type-safe wrapper.

[![Pub Package](https://img.shields.io/pub/v/firestore_ref.svg)](https://pub.dev/packages/firestore_ref)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)|||

---

### [theyakka/cumulus](https://github.com/theyakka/cumulus) `wrapper`

> Cumulus is a high-level framework that makes developing application logic on top of Firebase quick and simple.

this means: more abstract way to write NodeJS cloud functions.

platform support is given by its dependency to [pulyaevskiy/firebase-admin-interop](#pulyaevskiyfirebase-admin-interop-interop-library) and [pulyaevskiy/firebase-functions-interop](#pulyaevskiyfirebase-functions-interop-interop-library).

---

### [appsup-dart/firebase_dart](https://github.com/appsup-dart/firebase_dart) `native library`  

> A pure Dart implementation of the Firebase client

[![Pub Package](https://img.shields.io/pub/v/firebase_dart.svg)](https://pub.dev/packages/firebase_dart)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firebase|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Core|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [appsup-dart/firebase_admin](https://github.com/appsup-dart/firebase_admin) `native library`  

> A pure Dart implementation of the Firebase admin sdk

[![Pub Package](https://img.shields.io/pub/v/firebase_admin.svg)](https://pub.dev/packages/firebase_admin)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [appsup-dart/firebase_rest](https://github.com/appsup-dart/firebase_rest) `native library` [Discontinued]

> A Dart library for reading and writing data to a Firebase database.

[![Pub Package](https://img.shields.io/pub/v/firebase_rest.svg)](https://pub.dev/packages/firebase_rest)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firebase|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [appsup-dart/firebase_compute](https://github.com/appsup-dart/firebase_compute) `native library` [Discontinued]  

> Library for doing reactive computations with firebase.

[![Pub Package](https://img.shields.io/pub/v/firebase_compute.svg)](https://pub.dev/packages/firebase_compute)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|firebase_compute|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [amrfarid140/firebase_auth_oauth](https://github.com/amrfarid140/firebase_auth_oauth) `helper` `interop library`

> A Flutter plugin that makes it easy to perform OAuth sign in flows using FirebaseAuth. It also includes support for Sign in by Apple for Firebase. This plugin supports Android, iOS and Web. OAuth flows are performed by opening pop-up on top of the application to allow the user to authenticate or the native flow in the case of sign in by apple.

[![Pub Package](https://img.shields.io/pub/v/firebase_auth_oauth.svg)](https://pub.dev/packages/firebase_auth_oauth)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|firebase_auth_oauth|:white_check_mark:|:white_check_mark:|:white_check_mark:||||

[Auth Providers Support :link:](https://github.com/amrfarid140/firebase_auth_oauth/tree/main/firebase_auth_oauth#auth-providers-support)

---

### [lohanidamodar/flutter_firebase_helpers](https://github.com/lohanidamodar/flutter_firebase_helpers) `helper`

> A package that provides various Google Firebase related services helpers. Provides helpers to perform queries on firestore, firebase auth etc.

[![Pub Package](https://img.shields.io/pub/v/firebase_helpers.svg)](https://pub.dev/packages/firebase_helpers)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

--- 

### [duyduong/flutter_native_admob](https://github.com/duyduong/flutter_native_admob) `helper` `interop library`

> Plugin to integrate Firebase Native Admob to Flutter application Platform supported: iOS, Android

[![Pub Package](https://img.shields.io/pub/v/flutter_native_admob.svg)](https://pub.dev/packages/flutter_native_admob)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Admob|:white_check_mark:|:white_check_mark:|||||

--- 

### [jorgecoca/lumberdash](https://github.com/jorgecoca/lumberdash) `helper`

*lumberdash*  
> Do you need logs? Lumberdash is the answer! With a simple but powerful logging API, Lumberdash is the easiest way to record logs. And if that is not enough, you can extend its API and create your own custom plugins for your own logging needs.

*firebase_lumberdash* plugin  
> Plugin for lumberdash  
>  
> It sends your logs to Firebase Analytics.  

[![Pub Package](https://img.shields.io/pub/v/firebase_lumberdash.svg)](https://pub.dev/packages/firebase_lumberdash)

platform support is given by its dependency to [FirebaseExtended/flutterfire](#firebaseextendedflutterfire-interop-library).

---

### [GaspardMerten/Firebase-Cloud-Messaging-Interop](https://github.com/GaspardMerten/Firebase-Cloud-Messaging-Interop) `interop library`

> A dart plugin to use the Firebase Cloud Messaging Api (JS). You can retrieve the user's FCM token, delete it, access the notification data, ...

[![Pub Package](https://img.shields.io/pub/v/firebase_cloud_messaging_interop.svg)](https://pub.dev/packages/firebase_cloud_messaging_interop)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Messaging||||||:white_check_mark:|

---

### [jarekb123/firestore_all](https://github.com/jarekb123/firestore_all) `wrapper`

> Plugin that wraps Firestore from firebase and cloud_firestore packages and expose them as a single API.

[![Pub Package](https://img.shields.io/pub/v/firestore_all.svg)](https://pub.dev/packages/firestore_all)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:(macOs)||:white_check_mark:|

---

### [SwissCheese5/Dartbase-Admin-SDK](https://github.com/SwissCheese5/Dartbase-Admin-SDK) `native library`

> A dart-native implementation of the Firebase Admin SDK  
>  
> This library is a fork of cachapa's client firebase sdk; cachapa/firedart; modified and converted to support admin only firebase features. This library also uses these files from appsup-dart/firebase_admin to enable admin authentication to firebase because it is not documented on firebase's official documentation (May 2020):  
>- user_record.dart.
>- token_handler.dart

based on [cachapa/firedart](#cachapafiredart-native-library).

[![Pub Package](https://img.shields.io/pub/v/dartbase_admin.svg)](https://pub.dev/packages/dartbase_admin)

|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
|Firebase Auth|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Firestore|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Firebase Storage|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|
|Firebase Cloud Messaging|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|

---

### [kikuchy/lantern](https://github.com/kikuchy/lantern) `helper`

> Firebase Cloud Firestore's data structure definition language and code generator. Lantern lights bright future of your project.  
> ## Features  
> ### Definition Language  
> Have you ever been confused sharing collections / document structure in team? Or forgetting the structure by your self?  
>  
> No problem. Lantern is simple data structure definition language to write down your Firestore structure.  
...  
[more](https://github.com/kikuchy/lantern)  

[![Pub Package](https://img.shields.io/pub/v/lantern.svg)](https://pub.dev/packages/lantern)
