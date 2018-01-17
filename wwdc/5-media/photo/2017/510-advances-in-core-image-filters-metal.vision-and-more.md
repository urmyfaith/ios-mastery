# [Advances in Core Image: Filters, Metal, Vision, and More](https://developer.apple.com/videos/play/wwdc2017/510/)


2017-510-advances-in-core-image-filters-metal.vision-and-more.md


* Performance
  * Write CIKernels in Metal CIRenderDestination API
* Information
  * CIRenderInfo API Xcode Quick Looks
* Functionality


New Filters Barcode Support Depth Support

196

CIDepthToDisparity / CIDisparityToDepth CIMorphologyMinimum / Maximum / Gradient CIColorCubesMixedWithMask CIAreaMinMaxRed
CIDepthBlurEffect

CITextImageGenerator CIColorCurves CILabDeltaE CIBicubicScaleTransform CIBarcodeGenerator



## How to Create Metal CIKernels - by Tony 630



### Writing CIKernels in Metal (New)

Compiling

### Steps

•1. Write CIKernel in Metal shader file
•2. Compile and link Metal shader file
•3. Initialize CIKernel with function from Metal library

### Step 1 :

CIKernel Metal Library

2nd example: a color

3rd example: general.


New CIRenderDestination API 1905

Performance Benefits
Existing CIContext APIs for rendering to IOSurface or CVPixelBuffer
Return to caller when render is completed
•
New CIRenderDestination APIs
Return to caller when work is issued
•
This allows CPU and GPU work to be pipelined efficiently


```swift
// Clear Then Render Foreground Blended with Background
func renderImagePair (foregroundImage : CIImage, backgroundImage : CIImage, blend : CIBlendKernel = CIBlendKernel.sourceOver
toSurface : IOSurface)
{
  let dest = CIRenderDestination(ioSurface: toSurface)
  let ctx = getContext() // don’t create a context each time
  try? ctx.startTask(toClear: dest)
  try? ctx.startTask(toRender: backgroundImage, to: dest)
  dest.blendKernel = blend // use one of 37 built-in blend kernels or create your own try?
  ctx.startTask(toRender: foregroundImage, to: dest).waitUntilCompleted()
}
```


Rendering to Metal Drawable Textures

```swift
let ctx = getContext() // don’t create a context each time
let texture = currentDrawable.texture
let dest = CIRenderDestination(texture, commandBuffer: cmdBuffer) try? ctx.startTask(toRender: image, to: dest)
```


```swift
let ctx = getContext() // don’t create a context each time
while stillDrawing {
let dest = CIRenderDestination(
width: 1024,
height: 768,
pixelFormat: MTLPixelFormat.rgba8Unorm, commandBuffer: cmdBuffer) { () -> MTLTexture in
return currentDrawable.texture })
try? ctx.startTask(toRender: image, to: dest) }
```




Vision 3940


stabilization
