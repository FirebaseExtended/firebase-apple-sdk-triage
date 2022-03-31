# Building a sample app with Firebase via Carthage

[Carthage][carthage] is a dependency manager for Apple platforms that distributes
dependencies as binary frameworks.

## Getting started
Before continuing, ensure Carthage is installed on your machine by running:
```
which carthage
```
If the console prints `carthage not found`, you need to install Carthage.

### Installing Carthage
Carthage offers several [installation options][carthage-installing]. 

One option is to install it via [Homebrew][carthage-homebrew]:
```
brew install carthage
```

### 1. Configuring the `Cartfile`
Carthage pulls in dependencies based on the contents of a `Cartfile`. This is
similar to how CocoaPods uses a `Podfile` or Node.js uses a `Package.json`.

For convenience, there is a `Cartfile` with sample instructions at
[`./carthage/TriageApp/Cartfile`](/carthage/TriageApp/Cartfile). Please configure
this `Cartfile` with the Firebase products necessary to reproduce the issue.

### 2. Installing Firebase via Carthage
`cd` into [`./carthage/TriageApp/`](/carthage/TriageApp/) and then please start
from the second bullet and complete all the steps in the official
[Firebase Carthage integration instructions][firebase-carthage].

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
[carthage]: https://github.com/Carthage/Carthage
[carthage-homebrew]: https://formulae.brew.sh/formula/carthage
[carthage-installing]: https://github.com/Carthage/Carthage#installing-carthage
[firebase-carthage]: https://github.com/firebase/firebase-ios-sdk/blob/master/Carthage.md#carthage-usage
[firebase-console]: https://console.firebase.google.com/