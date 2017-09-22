# [Advances in Core Image: Filters, Metal, Vision, and More](https://developer.apple.com/videos/play/wwdc2017/510/)


2017-510-advances-in-core-image-filters-metal.vision-and-more.md


Performance
Write CIKernels in Metal CIRenderDestination API
Information
CIRenderInfo API Xcode Quick Looks
Functionality


New Filters Barcode Support Depth Support

196

CIDepthToDisparity / CIDisparityToDepth CIMorphologyMinimum / Maximum / Gradient CIColorCubesMixedWithMask CIAreaMinMaxRed
CIDepthBlurEffect

CITextImageGenerator CIColorCurves CILabDeltaE CIBicubicScaleTransform CIBarcodeGenerator



How to Create Metal CIKernels
•1. Write CIKernel in Metal shader file
•2. Compile and link Metal shader file
•3. Initialize CIKernel with function from Metal library

## Looking Inside Core Image
•Quick Look support and other runtime information
