# Firebase Triage Apps for the Firebase Apple SDK

This repo contains a collection of "skeleton" apps for quickly reproducing
issues from the [firebase-ios-sdk][firebase-ios-sdk].

There is a simple "skeleton" app for each supported distribution (i.e. CocoaPods)
and each of these apps offers several schemes to run on various Apple platforms
(i.e. tvOS) with different app lifecycle configurations.

In this context, a "skeleton" app is a basic, blank app with no custom logic that
has been created for a given platform (i.e. MacCatalyst).

## Getting started

### Prerequisite software
- Xcode (v13.2.1 or later)

You may need additional tooling depending on which app you're building:
- If building the app in the `cocoapods/` directory:
    - [CocoaPods][cocoapods] ([can be downloaded with Homebrew][cocoapods-homebrew])
- If building the app in the `carthage/` directory:
    - [Carthage][carthage] ([can be downloaded with Homebrew][carthage-homebrew])
- If building the app in the `zip/` directory:
    - A `Firebase.zip` downloaded from [Firebase Releases][firebase-releases]

### Clone this repo
Next, clone this repo onto your machine.

```
git clone git@github.com:google/firebaseappletriage.git
```

## Building a "skeleton" app
Each of the top-level directories contains documentation for how to build
its contained sample app for that given distribution method. Please refer to the
documentation there.

Provided within each directory is a single Xcode project called `TriageApp` with 5
targets:
|        Target Name       |           Lifecycle          | Supported Platforms |
|:------------------------ |:---------------------------- |:------------------- |
| SwiftUITriageApp (iOS)   | SwiftUI                      | iOS                 |
| SwiftUITriageApp (macOS) | SwiftUI                      | macOS               |
| SwiftUITriageApp (tvOS)  | SwiftUI                      | tvOS                |
| UIKitTriageApp           | UIKit                        | iOS, macCatalyst    |
| MixedUITriageApp         | UIApplicationDelegateAdaptor | iOS                 |

## License
The contents of this repository is licensed under the [Apache License, version 2.0][apache-license].

<!-- Links -->
[apache-license]: https://www.apache.org/licenses/LICENSE-2.0
[carthage]: https://github.com/Carthage/Carthage
[carthage-homebrew]: https://formulae.brew.sh/formula/carthage
[cocoapods]: https://cocoapods.org/
[cocoapods-homebrew]: https://formulae.brew.sh/formula/cocoapods
[firebase-ios-sdk]: https://github.com/firebase/firebase-ios-sdk
[firebase-releases]: https://github.com/firebase/firebase-ios-sdk/releases