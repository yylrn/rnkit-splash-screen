[![npm][npm-badge]][npm]
[![react-native][rn-badge]][rn]
[![MIT][license-badge]][license]
[![bitHound Score][bithound-badge]][bithound]
[![Downloads](https://img.shields.io/npm/dm/rnkit-splash-screen.svg)](https://www.npmjs.com/package/rnkit-splash-screen)

splashscreen for [React Native][rn].

[**Support me with a Follow**](https://github.com/simman/followers)

[npm-badge]: https://img.shields.io/npm/v/rnkit-splash-screen.svg
[npm]: https://www.npmjs.com/package/rnkit-splash-screen
[rn-badge]: https://img.shields.io/badge/react--native-v0.40-05A5D1.svg
[rn]: https://facebook.github.io/react-native
[license-badge]: https://img.shields.io/dub/l/vibe-d.svg
[license]: https://raw.githubusercontent.com/rnkit/rnkit-splash-screen/master/LICENSE
[bithound-badge]: https://www.bithound.io/github/rnkit/rnkit-splash-screen/badges/score.svg
[bithound]: https://www.bithound.io/github/rnkit/rnkit-splash-screen

## Getting Started

First, `cd` to your RN project directory, and install RNMK through [rnpm](https://github.com/rnpm/rnpm) . If you don't have rnpm, you can install RNMK from npm with the command `npm i -S rnkit-splash-screen` and link it manually (see below).

### iOS

* #### React Native < 0.46 (Using rnpm)

  `rnpm install rnkit-splash-screen@1.0.3`

* #### React Native >= 0.46
  `$npm install -S rnkit-splash-screen`

  `$react-native link rnkit-splash-screen`

#### Manually
1. Add `node_modules/rnkit-splash-screen/ios/RNKitSplashScreen.xcodeproj` to your xcode project, usually under the `Libraries` group
1. Add `libRNKitSplashScreen.a` (from `Products` under `RNKitSplashScreen.xcodeproj`) to build target's `Linked Frameworks and Libraries` list
1. Add ocr framework to `$(PROJECT_DIR)/Frameworks.`

### Android

* #### React Native < 0.46 (Using rnpm)

  `rnpm install rnkit-splash-screen@1.0.3`

* #### React Native >= 0.46
  `$npm install -S rnkit-splash-screen`

  `$react-native link rnkit-splash-screen`

#### Manually
1. JDK 7+ is required
1. Add the following snippet to your `android/settings.gradle`:

  ```gradle
include ':rnkit-splash-screen'
project(':rnkit-splash-screen').projectDir = new File(rootProject.projectDir, '../node_modules/rnkit-splash-screen/android/app')
  ```
  
1. Declare the dependency in your `android/app/build.gradle`
  
  ```gradle
  dependencies {
      ...
      compile project(':rnkit-splash-screen')
  }
  ```
  
1. Import `import io.rnkit.splashscreen.SplashScreenPackage;` and register it in your `MainActivity` (or equivalent, RN >= 0.32 MainApplication.java):

  ```java
  @Override
  protected List<ReactPackage> getPackages() {
      return Arrays.asList(
              new MainReactPackage(),
              new SplashScreenPackage(MainActivity.activity, true)
      );
  }
  ```

Finally, you're good to go, feel free to require `rnkit-splash-screen` in your JS files.

Have fun! :metal:

## Basic Usage

Import library

```
import RNKitSplashScreenManager from 'rnkit-splash-screen'
```

### TipText

```
RNKitSplashScreenManager.tipText('text')
```

### Progress

progress 0.0 .. 1.0, default is 0.0. values outside are pinned.

```
RNKitSplashScreenManager.progress(progress)
```

### Open

```
RNKitSplashScreenManager.open()
```

### Close

```
RNKitSplashScreenManager.close({animationType: RNKitSplashScreenManager.animationType.scale, duration: 850, delay: 500})
```

## Contribution

- [@simamn](mailto:liwei0990@gmail.com) The main author.

## Thanks

[@cyqresig](https://github.com/cyqresig) - [react-native-smart-splash-screen](https://github.com/react-native-component/react-native-smart-splash-screen)



## Questions

Feel free to [contact me](mailto:liwei0990@gmail.com) or [create an issue](https://github.com/rnkit/rnkit-splash-screen/issues/new)

> made with ♥