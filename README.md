<p align="center">
  <img src="http://yannickloriot.com/resources/dynamicfont-header.png" alt="DynamicFont">
</p>

<p align="center">
  <a href="http://cocoadocs.org/docsets/DynamicFont/"><img alt="Supported Platforms" src="https://cocoapod-badges.herokuapp.com/p/DynamicFont/badge.svg"/></a>
  <a href="http://cocoadocs.org/docsets/DynamicFont/"><img alt="Version" src="https://cocoapod-badges.herokuapp.com/v/DynamicFont/badge.svg"/></a>
  <a href="https://github.com/Carthage/Carthage"><img alt="Carthage compatible" src="https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat"/></a>
  <a href="https://travis-ci.org/yannickl/DynamicFont"><img alt="Build status" src="https://travis-ci.org/yannickl/DynamicFont.svg?branch=master"/></a>
  <a href="http://codecov.io/github/yannickl/DynamicFont"><img alt="Code coverage status" src="http://codecov.io/github/yannickl/DynamicFont/coverage.svg?branch=master"/></a>
  <a href="https://codebeat.co/projects/github-com-yannickl-dynamicfont"><img alt="Codebeat badge" src="https://codebeat.co/badges/54d768e5-9e35-4c8a-9893-bcf519756215" /></a>
</p>

**DynamicFont** provides powerful methods to manipulate font in an easy way in Swift.

<p align="center">
    <a href="#requirements">Requirements</a> • <a href="#usage">Usage</a> • <a href="#installation">Installation</a> • <a href="#contact">Contact</a> • <a href="#license-mit">License</a>
</p>

## Requirements

- iOS 10.0+
- Xcode 8.0+
- Swift 3.0+

## Usage

To begin, let's start with the font creation thanks to a `DynamicFontFamily`:

```swift
import DynamicFont

// Helvetica Font
let helvetica = DynamicFont(family: .helvetica, size: 12)
// Equivalent to
// let helvetica = UIFont(family: .helvetica, size: 12)
```
*Notice that the initializer returns a font and not an optional like the designated UIFont initializer*

Now you can transform your font appearance by modifying its size or by italicizing it:

```swift
// Helvetica-Bold
let bold = helvetica.withWeight(.bold)

// Helvetica-BoldOblique
let boldItalic = bold.withItalic()
```

You can change the weight of the font by picking one of this case:

```swift
enum DynamicFontWeight {
  /// The ultra light font weight.
  case ultraLight
  /// The thin font weight.
  case thin
  /// The light font weight.
  case light
  /// The regular font weight.
  case regular
  /// The medium font weight.
  case medium
  /// The semibold font weight.
  case semibold
  /// The bold font weight.
  case bold
  /// The heavy font weight.
  case heavy
  /// The black font weight.
  case black
}
```

#### And many more...

To go further, take a look at the example project.

## Installation

#### CocoaPods

Install CocoaPods if not already available:

``` bash
$ [sudo] gem install cocoapods
$ pod setup
```
Go to the directory of your Xcode project, and Create and Edit your *Podfile* and add _DynamicFont_:

``` bash
$ cd /path/to/MyProject
$ touch Podfile
$ edit Podfile
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'

use_frameworks!
pod 'DynamicFont', '~> 1.0.1'
```

Install into your project:

``` bash
$ pod install
```

Open your project in Xcode from the .xcworkspace file (not the usual project file):

``` bash
$ open MyProject.xcworkspace
```

You can now `import DynamicFont` framework into your files.

#### Carthage

[Carthage](https://github.com/Carthage/Carthage) is a decentralized dependency manager that automates the process of adding frameworks to your Cocoa application.

You can install Carthage with [Homebrew](http://brew.sh/) using the following command:

```bash
$ brew update
$ brew install carthage
```

To integrate `DynamicFont` into your Xcode project using Carthage, specify it in your `Cartfile` file:

```ogdl
github "yannickl/DynamicFont" >= 1.0.1
```

#### Swift Package Manager
You can use [The Swift Package Manager](https://swift.org/package-manager) to install `DynamicFont` by adding the proper description to your `Package.swift` file:
```swift
import PackageDescription

let package = Package(
    name: "YOUR_PROJECT_NAME",
    targets: [],
    dependencies: [
        .Package(url: "https://github.com/yannickl/DynamicFont.git", versions: "1.0.1" ..< Version.max)
    ]
)
```

Note that the [Swift Package Manager](https://swift.org/package-manager) is still in early design and development, for more information checkout its [GitHub Page](https://github.com/apple/swift-package-manager).

#### Manually

[Download](https://github.com/YannickL/DynamicFont/archive/master.zip) the project and copy the `DynamicFont` folder into your project to use it in.

## Contact

Yannick Loriot
 - [https://21.co/yannickl/](https://21.co/yannickl/)
 - [https://twitter.com/yannickloriot](https://twitter.com/yannickloriot)

## License (MIT)

Copyright (c) 2016-present - Yannick Loriot

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
