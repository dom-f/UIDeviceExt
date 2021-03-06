# UIDeviceExt
`UIDeviceExt` provide class methods to get information about pixels-per-centimeter/inch and points-per-centimeter/inch of an iPod, iPhone or iPad. This information can be used to render graphics that has dimensions of known size in centimeters/inches, etc.

A demo shows how this can be used to simulate 1 mm graph-paper on any iPod, iPhone or iPad (best on Retina displays).

![screenshot](https://github.com/marchv/UIDeviceExt/blob/master/screenshot.png?raw=true)

The interface is simply:

    @interface UIDeviceExt : NSObject

    + (float)pointsPerCentimeter;
    + (float)pixelsPerCentimeter;

    + (float)pointsPerInch;
    + (float)pixelsPerInch;

    @end

For example this can be used like this:

    #import "UIDeviceExt.h"
    float pointsPerMillimeter = [UIDeviceExt pointsPerCentimeter] * 0.1f;

## Please note
Whenever a new iPod, iPhone or iPad gets released this code has to be updated. If not new devices will fail to derive the information!

## Requirements
`UIDeviceExt` has only been tested on iOS 7.1 but I assume it should be fine on any iOS version. Please note that the demo program requires ARC.

## Installation
In Xcode add the `UIDeviceExt` subdirectory including the two files `UIDeviceExt.h` and `UIDeviceExt.m` from this repo into your project.
