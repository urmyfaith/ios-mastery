# looking-inside-core-image--david--2700.md





## Looking Inside Core Image - David 2700

•Quick Look support and other runtime information



// load image and apply orientation
var image = CIImage( contentsOf: url
options: [kCIImageApplyOrientationProperty: true])
// downsample by 2x
image = image.applying(CGAffineTransform(scaleX:0.5, y:0.5))
