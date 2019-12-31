# PackageInfo

This Flutter plugin provides an API for querying information about an
application package.

# Usage

You can use the PackageInfo to query information about the
application package. This works both on iOS and Android.

```dart
import 'package:package_info/package_info.dart';

PackageInfo packageInfo = await PackageInfo.fromPlatform();

String appName = packageInfo.appName;
String packageName = packageInfo.packageName;
String version = packageInfo.version;
String buildNumber = packageInfo.buildNumber;
```

Or in async mode:

```dart
PackageInfo.fromPlatform().then((PackageInfo packageInfo) {
  String appName = packageInfo.appName;
  String packageName = packageInfo.packageName;
  String version = packageInfo.version;
  String buildNumber = packageInfo.buildNumber;
});
```

## Known Issue

As noted on [issue 20761](https://github.com/flutter/flutter/issues/20761#issuecomment-493434578), package_info on iOS 
requires the Xcode build folder to be rebuilt after changes to the version string in `pubspec.yaml`. 
Clean the Xcode build folder with: 
`XCode Menu -> Product -> (Holding Option Key) Clean build folder`. 

## Issues and feedback

Please file [issues](https://github.com/flutter/flutter/issues/new) to send feedback or report a bug. Thank you!
