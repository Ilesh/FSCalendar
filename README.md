
![fscalendar](https://cloud.githubusercontent.com/assets/5186464/6655324/213a814a-cb36-11e4-9add-f80515a83291.png)<br/><br/>
[![Version](https://img.shields.io/cocoapods/v/FSCalendar.svg?style=flat)](http://cocoadocs.org/docsets/FSCalendar)
[![License](https://img.shields.io/cocoapods/l/FSCalendar.svg?style=flat)](http://cocoadocs.org/docsets/FSCalendar)
[![Platform](https://img.shields.io/cocoapods/p/FSCalendar.svg?style=flat)](http://cocoadocs.org/docsets/FSCalendar)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)

![fscalendar](https://cloud.githubusercontent.com/assets/5186464/10262249/4fabae40-69f2-11e5-97ab-afbacd0a3da2.jpg)

# Installation

## Cocoapods:

* For iOS8+: 👍
```ruby
use_frameworks!
pod 'FSCalendar'
```

* For iOS7+:
```ruby
pod 'FSCalendar'
```

## Carthage:
* For iOS8+
```ruby
github "WenchaoIOS/FSCalendar"
```

## Manually:
* Drag all files under `FSCalendar` folder into your project. 👍

## Support IBInspectable / IBDesignable
Only the methods marked "👍" support IBInspectable / IBDesignable feature. [Have fun with Interface builder](#roll_with_interface_builder)

# Setup

## Use Interface Builder (Recommended)

1. Drag an UIView object to ViewController Scene
2. Change the `Custom Class` to `FSCalendar`<br/>
3. Link `dataSource` and `delegate` to the ViewController <br/>

![fscalendar-ib](https://cloud.githubusercontent.com/assets/5186464/9488580/a360297e-4c0d-11e5-8548-ee9274e7c4af.jpg)

4. Finally, you should implement `FSCalendarDataSource` and `FSCalendarDelegate` in ViewController.m

## Or use code

```objective-c
@property (weak , nonatomic) FSCalendar *calendar;
```
```objective-c
// In loadView or viewDidLoad
FSCalendar *calendar = [[FSCalendar alloc] initWithFrame:CGRectMake(0, 0, 320, 300)];
calendar.dataSource = self;
calendar.delegate = self;
[self.view addSubview:calendar];
self.calendar = calendar;
```
<br/>

## Or swift

* To use `FSCalendar` in swift, you need to [Create Bridge Header](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/BuildingCocoaApps/MixandMatch.html) first.


```swift
private weak var calendar: FSCalendar!
```
```swift
// In loadView or viewDidLoad
let calendar = FSCalendar(frame: CGRect(x: 0, y: 0, width: 320, height: 300))
calendar.dataSource = self
calendar.delegate = self
view.addSubview(calendar)
self.calendar = calendar
```
### <a id="roll_with_interface_builder"></a> Roll with Interface Builder
![fscalendar - ibdesignable](https://cloud.githubusercontent.com/assets/5186464/9301716/2e76a2ca-4503-11e5-8450-1fa7aa93e9fd.gif)

## More Usage
* To view more usage, download the zip file and read the example.
* Or your could refer to [this document](https://github.com/WenchaoIOS/FSCalendar/blob/master/MOREUSAGE.md)

# License
FSCalendar is available under the MIT license. See the LICENSE file for more info.
