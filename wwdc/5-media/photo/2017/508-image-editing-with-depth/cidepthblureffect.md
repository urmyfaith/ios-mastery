

## [Using CIDepthBlurEffect - Alexandre Naaman, Technical Lead, Core Image](cidepthblureffect.md)


```swift
let mainImage =CIImage(contentsOf: url)


let disparityImage = CIImage(contentsOf: url, options: [kCIImageAuxiliaryDisparity
true])

let filter = CIFilter(name :  "CIDepthBlurEffect", withInputParameters: [])

var resultImage = filter.outputImage


```

### Additional Reminders
