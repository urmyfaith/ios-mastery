# [2017 506 Vision Framework: Building on Core ML](https://developer.apple.com/videos/play/wwdc2017/506/)

506-vision-framework-building-on-core-ml.md


No | Topic | Presenter | Time
--|--|--|--
1|What Can Vision Do|
2|Vision Concepts| Frank Doepke | 815
3|The Code|

## What Can Vision Do

* Face Landmarks, smaller face, strong profile,
  * Face Landmarks
* Image Registration
* Rectangle Detection
* Barcode Detection
* Text Detection
* Object Tracking
  * For faces, rectangles, and general templates
* Integration with Core ML

### On Devices vs. Cloud


## Vision Concepts - Frank - 815


concept | class
--|--
The Asks | Request
The Machinery | Handler
The Results | Observation


## The code



```swift
// Create request
 let = VNDetectFaceRectanglesRequest()
faceDetectionRequest
// Create request handler
let myRequestHandler =
// send the requests to the request handler
(url: fileURL, options: [:])
VNImageRequestHandler
myRequestHandler.perform([faceDetectionRequest])
// Do we have a face
for observation in faceDetectionRequest.results as! [VNFaceObservation] { }

```

### Sequence

```swift
// Create a sequence request handler
let requestHandler = ()
let observations = detectionRequest. as! [VNDetectedObjectObservation]
let objectsToTrack = observations.map { VNTrackObjectRequest(detectedObjectObservation: $0) }
// Run the requests
requestHandler.perform(objectsToTrack, on: pixelBuffer)
// Lets look at the results
for request in objectsToTrack
for observation in request.results as! [VNDetectedObjectObservation]
```



## Best Practices


Envisioning a Vision Task

* which image type is right for me?
* what am i going to do with the image?
* what performance do I need or want?

### Which Image Type Is Right for Me?

* Vision supports various image types
  * CVPixelBufferRef CGImageRef CIImage
  * NSURL
  * NSData
* The image type to choose depends on where the image comes from
* You shouldn’t have to pre-scale the image
* Make sure to pass in the EXIF orientation of the image

## Everything streaming

CVPixelBuffer


## Files from Disk or Web
