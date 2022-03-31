# Building a sample app with Firebase via Swift Package Manager

[Swift Package Manager][swift-package-manager] (SPM) is a dependency manager that
comes out of the box with Xcode.

### 1. Open the Xcode project in [`./swift_package_manager/TriageApp/`](/swift_package_manager/TriageApp/)

From the command line:
```
cd ./swift_package_manager/TriageApp/
xed .
```

### 2. Complete the SPM integration instructions
Please read and complete the official 
[Firebase SPM integration instructions][firebase-spm-integration].

### 2. Configuring the `GoogleService-Info.plist`
The sample app targets contain a fake `GoogleService-Info.plist`. 

For triaging issues that do **not** involve Firebase backend, this should be
sufficient.

Otherwise, you'll need to create a Firebase project on the
[Firebase Console][firebase-console] and replace the fake 
`GoogleService-Info.plist` with the one generated for you on the console. Use
`com.google.firebase.triageapp` as the bundle ID when prompted during the project
setup flow.

### Next steps
At this point, the Firebase should be integrated into the sample app. Please
select a target to build and run.

<!-- Links -->
[firebase-console]: https://console.firebase.google.com/
[firebase-spm-integration]: https://github.com/firebase/firebase-ios-sdk/blob/master/SwiftPackageManager.md
[swift-package-manager]: https://swift.org/package-manager/

