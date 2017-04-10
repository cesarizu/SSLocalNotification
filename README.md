# SSLocalNotification

[![CI Status](http://img.shields.io/travis/nickdbellucci@gmail.com/SSLocalNotification.svg?style=flat)](https://travis-ci.org/nickdbellucci@gmail.com/SSLocalNotification)
[![Version](https://img.shields.io/cocoapods/v/SSLocalNotification.svg?style=flat)](http://cocoapods.org/pods/SSLocalNotification)
[![License](https://img.shields.io/cocoapods/l/SSLocalNotification.svg?style=flat)](http://cocoapods.org/pods/SSLocalNotification)
[![Platform](https://img.shields.io/cocoapods/p/SSLocalNotification.svg?style=flat)](http://cocoapods.org/pods/SSLocalNotification)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements
* ARC
* iOS8

## Installation

SSLocalNotification is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "SSLocalNotification"
```

## Usage

* Basic Notification

```Swift

import BlinkingLabel

let notification = SSLocalNotificationController(title: "SSLocalNotification", message: "This is a test notification!", preferredStyle: .light)
notification.image = UIImage()
notification.setTitleFont(fontName: "Avenir-Medium", color: .black)
notification.setMessageFont(fontName: "Avenir-Book", color: .black)
notification.presentLocalNotification()

```

* Add Actions

```Swift

notification.addAction(action: SSLocalNotificationAction(title: "Button 1", fontName: "Avenir-Book", tint: .blue, handler: {
    print("Custom Action")
}))
notification.addAction(action: SSLocalNotificationAction(title: "Button 2", fontName: "Avenir-Book", tint: .blue, handler: {
    print("Custom Action")
}))

```

* Further Customization

```Swift

// Make the notification expandable
notification.expandable = true

// Change how long the notification is presented
notification.dismissDelay = 4.0

// Add action when user taps the notification
notification.didTapLocalNotification = tapFunction()

// Add action when user dismisses the notification
notification.didTapLocalNotification = dismissFunction()

```


* ARC

## Author

nickdbellucci@gmail.com

## License

SSLocalNotification is available under the MIT license. See the LICENSE file for more info.
