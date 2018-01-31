# looking-inside-core-image--david--2700.md

## Looking Inside Core Image - David 2700

•Quick Look support and other runtime information



```swift
// load image and apply orientation
var image = CIImage( contentsOf: url
options: [kCIImageApplyOrientationProperty: true])
// downsample by 2x
image = image.applying(CGAffineTransform(scaleX:0.5, y:0.5))
```




### CIImage Quick Look

```swift
// load disparity image and apply orientation
var disparity = CIImage(
contentsOf: url,
options: [kCIImageAuxiliaryDisparity: true,
kCIImageApplyOrientationProperty: true]) // cubic upsample by 2x
disparity = disparity.applyingFilter(“CIBicubicScaleTransform”, withInputParameters: [...])
// adjust disparity mask and blend foreground and background
let mask = disparity.applyingFilter(“CIColorControls", withInputParameters: [kCIInputContrastKey: 2.0])
mask = mask.applyingFilter(“CIColorClamp")
```

### CIImage Quick Look

```swift

// adjustment for foreground
let fg = image.applyingFilter("CIPhotoEffectFade") // adjustment for background
let bg = image.applyingFilter("CIPhotoEffectNoir")
// combine foreground and background using mask
let output = fg.applyingFilter("CIBlendWithMask", withInputParameters: [ kCIInputBackgroundImageKey: bg,
kCIInputMaskImageKey: mask])

```

### CIRenderTask Quick Look

```swift

// render output to an IOSurface
let dest = CIRenderDestination(ioSurface: surface);
let context = self.context;
guard
let task = try? context.startTask(toRender: output, to: dest),
let info = try? task.waitUntilCompleted() else {
// handle render failure
}
```

### CIRenderInfo Quick Look

```swift

// render output to an IOSurface
let dest = CIRenderDestination(ioSurface: surface);
let context = self.context;
guard
  let task = try? context.startTask(toRender: output, to: dest),
  let info = try? task.waitUntilCompleted()
else {
  // handle render failure
}

```
