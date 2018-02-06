
## Best Practices


Envisioning a Vision Task

* which image type is right for me?
* what am i going to do with the image?
* what performance do I need or want?

### Which Image Type Is Right for Me?

* Vision supports various image types
  * CGImage/CGImageRef
  * CIImage
  * CVPixelBuffer/CVPixelBufferRef
  * URL/NSURL
  * Data/NSData
* The image type to choose depends on where the image comes from
* You shouldn’t have to pre-scale the image
* Make sure to pass in the EXIF orientation of the image

## Everything streaming

CVPixelBuffer


## Files from Disk or Web

* URL for image files on disk
* NSData for images from the web
* Least amount of memory footprint
* Vision will do the scaling without reading the full image if possible
* EXIF Orientation is derived from the file if possible but can be overwritten



### Face Detector Landscape

X | Vision | Core Image | AV Capture
--|--|--|--
Accuracy|Best|Better|Good
Processing time|Fast|Faster|Fastest
Power usage|Good|Better|Best
Availability|iOS, macOS, tvOS|iOS, macOS, tvOS|iOS only
