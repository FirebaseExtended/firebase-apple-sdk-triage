# Building a sample app with Firebase via Zip

Firebase provides a pre-built binary `XCFramework` distribution for users who want to integrate Firebase without using a dependency manager.

### 1. Download a Firebase release
Download a `Firebase.zip` from [Firebase Releases][firebase-releases]. You can find the zip for all Firebase releases there.

### 2. Complete the manual integration instructions
Uncompressing the downloaded zip will reveal a `README.md` with instructions on how to integrate Firebase into your app. These instructions can also be found [here][firebase-zip-integration]. 

Use the [`./zip/TriageApp/`](/zip/TriageApp/) directory as the working directory in which you complete the integration steps.

### 3. Configuring the `GoogleService-Info.plist`
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
[firebase-zip-integration]: https://github.com/firebase/firebase-ios-sdk/blob/master/ReleaseTooling/Template/README.md#integration-instructions