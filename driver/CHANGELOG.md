# Changelog

## 1.14.1
- Bump the UIA2 version

## 1.14.0
- Fix proxyCommand for plugins [#425](https://github.com/appium-userland/appium-flutter-driver/pull/425)
- Fix startNewCommandTimeout call [#426](https://github.com/appium-userland/appium-flutter-driver/pull/426)

## 1.13.1
- Fix no `waitTimeoutMilliseconds` argument case for scrollUntilVisible/scrollUntilTapable

## 1.13.0
- Add arguments in scrollUntilVisible/scrollUntilTapable
    - `waitTimeoutMilliseconds`: The timeout to try scroll up to the timeout
    - `durationMilliseconds`: The duration to do a scroll action. `timeout` in [scroll](https://api.flutter.dev/flutter/flutter_driver/FlutterDriver/scroll.html).
    - `frequency`: The frequency to for the move events in  [scroll](https://api.flutter.dev/flutter/flutter_driver/FlutterDriver/scroll.html).


## 1.12.0
- Support `setClipboard` and `getClipboard` by always proxying the request to the NATIVE_APP context
- Support non-`app` and non-`bundleId` nor non-`appPackage` session starts as `FLUTTER` context
- Add `installApp` to install the test target after the new session request

## 1.11.0
- Add `activateApp` support to start an app

## 1.10.0
- Add `terminateApp` support to stop the running application
    - The behavior is the same as when you call the same endpoint in NATIVE_APP context

## 1.9.1
- Improved error message when no observatory url found

## 1.9.0
- **Breaking change**
    - Revert [#306](https://github.com/appium-userland/appium-flutter-driver/pull/306) (added in v1.5.0). `scrollUntilVisible` uses `waitFor` as same as before v1.5.0.
        - Please use `scrollUntilTapable` instead since this version
 - Added `scrollUntilTapable` command to scroll with `waitForTappable` [#360](https://github.com/appium-userland/appium-flutter-driver/pull/360)

## 1.8.0

Appium `2.0.0-beta.46` and higher is needed as dependencies update in dependent Appium UIA2/XCUITest drivers

- Added `timeout` argument for scrollIntoView [#358](https://github.com/appium-userland/appium-flutter-driver/pull/358)
- Added `skipPortForward` capability [#343](https://github.com/appium-userland/appium-flutter-driver/pull/343)

## 1.7.2 (1.7.1)
- Fixed `* 1000` in `scroll` [#330](https://github.com/appium-userland/appium-flutter-driver/pull/330)

## 1.7.0
- **Breaking change**
    - Do not calculate `* 1000` internally for milliseconds arguments to set them properly as same as README/examples. [#319](https://github.com/appium-userland/appium-flutter-driver/issues/319)

## 1.6.0
- Update for newer Appium 2 beta

## 1.5.0

- Use `waitForTappable` in `scrollUntilVisible` [#306](https://github.com/appium-userland/appium-flutter-driver/pull/306)

## 1.4.0

- Added `flutter:getIsolate` to get the isolate information [#298](https://github.com/appium-userland/appium-flutter-driver/pull/298)

## 1.3.0

- Added `flutter:getVMInfo` and `flutter:setIsolateId` commands to allow a session to switch the target isolate id [#292](https://github.com/appium-userland/appium-flutter-driver/pull/292)

## 1.2.0

- Added `waitForTappable` [#289](https://github.com/appium-userland/appium-flutter-driver/pull/289)

## 1.1.2 (1.1.1)

- Fixed checking observatory URL every trial [#287](https://github.com/appium-userland/appium-flutter-driver/pull/287)

## 1.1.0

- Support processLogToGetobservatory for Flutter >= 3.0.0 [#283](https://github.com/appium-userland/appium-flutter-driver/pull/283)
