# GSMessages

Easy to use messages/notifications for iOS written in pure Swift. Inspired from [TSMessages](https://github.com/KrauseFx/TSMessages)

![](https://github.com/wxxsw/GSMessages/blob/master/demo.gif)

## Example

To show notifications use the following code:
```Swift
self.showMessage("Something success", type: .Success, options: nil)
```

To display a notice on a view:
```Swift
view.showMessage("Something success", type: .Success, options: [.Position(.Bottom)])
```

To hide a notification manually:
```Swift
self.hideMessage()
```

##### Parameters:

```Swift
self.showMessage("Some Text...", 
                 type: .Success,                    // .Success || .Error || .Warning || .Info 
                 options: [.Animation(.Slide),        // .Slide || .Fade
                           .AnimationDuration(0.3),
                           .AutoHide(true),
                           .AutoHideDelay(3.0),
                           .Height(44.0),
                           .Position(.Top),             // .Top || .Bottom
                           .TextColor(.whiteColor())]
```

## Font / Background Color

To set custom fonts and background colors in the following ways:
```Swift
GSMessage.font = UIFont.boldSystemFontOfSize(12)
GSMessage.successBackgroundColor = .greenColor()
GSMessage.warningBackgroundColor = .yellowColor()
GSMessage.errorBackgroundColor = .redColor()
GSMessage.infoBackgroundColor = .blueColor()
```

## Requirements

- iOS 7.0+
- Xcode 6.4 (Swift 1.2)

## Installation

> **Embedded frameworks require a minimum deployment target of iOS 8.**
>
> To use GSMessages with a project targeting iOS 7, you must to drag `GSMessage.swift` to your iOS Project.

### [CocoaPods](http://cocoapods.org/):

In your `Podfile`:
```
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'
use_frameworks!

pod "GSMessages"
```

And in your `*.swift`:
```swift
import GSMessages
```

## License

GSMessages is available under the MIT license. See the LICENSE file for more info.
