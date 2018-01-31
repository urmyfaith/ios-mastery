
# [2017 510 Advances in Core Image](https://developer.apple.com/videos/play/wwdc2017/510/)

> Filters, Metal, Vision, and More

No|Topic|Presenter|Time|Page
--|--|--|--|--
0|Recap|
1|New Built-In CIFilters|David|
2|CIKernel in Metal|Tony|630
3|[New CIRenderDestination API](CIRenderDestination.md) |Tony|1905|p83
4|Look Inside|David|2700
5|CIBarcodeDescriptor|David|3515
6|Vision + Demo|David, Skye|3940


## Summary of What’s New

Our goal for this release is to enable developers to get better:

* Performance
  * Write CIKernels in Metal
  * CIRenderDestination API
* Information
  * CIRenderInfo API
  * Xcode Quick Looks
* Functionality
  * New Filters
  * Barcode Support
  * Depth Support


## New Built-In CIFilters

### 196


### New Built-In CIFilters - Some that are useful for Depth filtering

* CIDepthToDisparity / CIDisparityToDepth
* CIMorphologyMinimum / Maximum / Gradient
* CIColorCubesMixedWithMask
* CIAreaMinMaxRed
* CIDepthBlurEffect

### New Built-in CIFilters - Some that are often requested additions

* CITextImageGenerator
* CIColorCurves
* CILabDeltaE
* CIBicubicScaleTransform
* CIBarcodeGenerator

### New Built-in CIFilters - Some that are improved

* CIHueBlendMode
* CISaturationBlendMode
* CIColorBlendMode
* CILuminosityBlendMode
* CILinearBurnBlendMode

The demosaic and noise reduction filters used for RAW files



## [CIKernels-in-Metal.md](CIKernels-in-Metal.md) -  Tony  - 630

## [New CIRenderDestination API](CIRenderDestination.md) 1905


## [Vision](vision--david--3940.md) - David -  3940
