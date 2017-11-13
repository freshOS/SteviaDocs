# Installation

### CocoaPods
```swift
pod 'SteviaLayout'
use_frameworks!
```

### Carthage
```swift
github "freshOS/Stevia"
```

- Create a `Cartfile` file at the root of your project folder

- Add `github "freshOS/Stevia"` to your Cartfile

- Run `carthage update`

- Drag and drop `Stevia.framework` from `/Carthage/Build/iOS/` to Linked frameworks and libraries in Xcode (Project>Target>General>Linked frameworks and libraries)

- Add new run script (Project>Target>Build Phases>+> New run script phase) `/usr/local/bin/carthage copy-frameworks`

- Add Input files `$(SRCROOT)/Carthage/Build/iOS/Stevia.framework`

There you go!

### Manual
Copy Stevia source files to your Xcode project
