# [![Yuneec](http://developer.yuneec.com/sites/default/files/docs/YuneecLogo.svg)](https://developer.yuneec.com)

# Yuneec SDK for iOS

iOS wrappers for the Yuneec-SDK https://github.com/YUNEEC/Yuneec-SDK written in Objective-C/Objective-C++.

## Usage

### Use Carthage to get the framework

To use the Yuneec SDK in your iOS application, you can pull in this framework using [Carthage](https://github.com/Carthage/Carthage).

To install carthage, it's easiest to use [Homebrew](https://brew.sh/):

```
brew install carthage
```

Then to add the framework, create the file `Cartfile` in your app's repository with below's content:

```
# Require the iOS framework of the Yuneec SDK
github "YUNEEC/Yuneec-SDK-iOS" >= 0.3.1
```

Then, to pull in the library and build it, run Carthage in your app's repository:

```
carthage update --use-ssh
```

This command also needs to be re-run if you want to udpate the framework.

### Add the framework into your project

Open the project in XCode and do the following:

1. Open Project Settings -> General
2. Find Embedded Binaries and press *+*
3. Click Other, go one folder up, and select `Carthage/Build/iOS/Yuneec_SDK_iOS.framework`.
4. Do "Product Clean" and "Product Build"

### Use Carthage to check out a developer branch

While developing, you might need a developer version of the iOS wrappers. They can be accessed by using a branch in the `Cartfile`:

```
github "YUNEEC/Yuneec-SDK-iOS" "branch-name"
```

## Docs

Autogenerated API docs can be found in the [docs](docs/) directory.

### Generate docs

To generate the docs, [jazzy](https://github.com/realm/jazzy) is used.

To install it, do:

```
sudo gem install jazzy
```

To update the docs:

```
jazzy --objc --umbrella-header Yuneec_SDK_iOS/Yuneec_SDK_iOS.h --theme docs/yuneec
```

## License

The source code in this repository which is just a  wrapper around the Yuneec-SDK (C++ library) is published under the [BSD 3-Clause license](LICENSE).
