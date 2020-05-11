# State of Firebase for Dart
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

## packages

### FirebaseExtended/flutterfire
|Product|Flutter iOS|Flutter Android|Flutter Web|Flutter Desktop|native (VM & Fuchsia)|dart2js|
|---|---|---|---|---|---|---|
| [cloud_firestore](https://pub.dev/packages/cloud_firestore)|:white_check_mark:|:white_check_mark:|:white_check_mark:|:white_check_mark:|:negative_squared_cross_mark:|:negative_squared_cross_mark:|
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
