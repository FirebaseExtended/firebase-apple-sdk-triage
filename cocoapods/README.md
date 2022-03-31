# Building a sample app with Firebase via CocoaPods

[CocoaPods][cocoapods] is a dependency manager for Apple platforms that distributes
dependencies as defined in a given [`podspec`][cocoapods-podspec].

## Getting started
Before continuing, ensure CocoaPods is installed on your machine by running:
```
which pod
```
If the console prints `pod not found`, you need to install CocoaPods.

### Installing CocoaPods
CocoaPods offers several [installation options][cocoapods-installing]. 

One option is to install it via [Homebrew][cocoapods-homebrew]:
```
brew install CocoaPods
```

### 1. Configuring the `Podfile`
CocoaPods pulls in dependencies based on the contents of a
[`Podfile`][cocoapods-podfile]. This is similar to how Node.js uses
a `Package.json`.

For convenience, there is a `Podfile` with sample instructions at
[`./cocoapods/TriageApp/Podfile`](/cocoapods/TriageApp/Podfile). Please configure
this `cocoapods` with the Firebase products necessary to reproduce the issue.

### 2. Installing Firebase via CocoaPods
`cd` into [`./cocoapods/TriageApp/`](/cocoapods/TriageApp/). Then, install the
dependencies and open the resulting *.xcworkspace in Xcode with:
```
pod install --repo-update
xed .
```

Additionally, for some products (i.e. Crashlytics), additional setup is
[required][[firebase-cocoapods-extra]].

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
[cocoapods]: https://cocoapods.org/
[cocoapods-homebrew]: https://formulae.brew.sh/formula/cocoapods
[cocoapods-installing]: https://guides.cocoapods.org/using/getting-started.html
[cocoapods-podfile]: https://guides.cocoapods.org/syntax/podfile.html
[cocoapods-podspec]: https://guides.cocoapods.org/syntax/podspec.html
[firebase-cocoapods-extra]: https://firebase.google.com/docs/ios/installation-methods#product-specific-considerations
[firebase-console]: https://console.firebase.google.com/