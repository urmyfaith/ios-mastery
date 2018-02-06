# [2017 506 Vision Framework: Building on Core ML](https://developer.apple.com/videos/play/wwdc2017/506/)

506-vision-framework-building-on-core-ml.md


No | Topic | Presenter | Time|Page
--|--|--|--
1|What Can Vision Do|
2|Vision Concepts| Frank Doepke | 815
3|The Code|
4|[Best Practices](best-practice.md)|
5|Show And Tell||1930|p77


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


Analyzing an Image

Tracking in a Sequence

### Image Request Handler

* For interactive exploration of an image
* Holds on to the image for its lifecycle
* Allows optimization of various requests performed on an image

### Sequence Request Handler

* For anything that looks at images in a sequence like tracking
* Does not optimize for multiple requests on an image

## Putting It into Code


```swift
// Create request
let faceDetectionRequest = VNDetectFaceRectanglesRequest()

// Create request handler
let myRequestHandler = VNImageRequestHandler(url: fileURL, options: [:])

// send the requests to the request handler
myRequestHandler.perform([faceDetectionRequest])

// Do we have a face
for observation in faceDetectionRequest.results as! [VNFaceObservation] {

}

```

### Sequence

```swift
// Create a sequence request handler
let requestHandler =  VNSequenceRequestHandler()


// Start the tracking with an observation
let observations = detectionRequest.results as! [VNDetectedObjectObservation]
let objectsToTrack = observations.map { VNTrackObjectRequest(detectedObjectObservation: $0) }

// Run the requests
requestHandler.perform(objectsToTrack, on: pixelBuffer)

// Lets look at the results
for request in objectsToTrack {
  for observation in request.results as! [VNDetectedObjectObservation] {

  }
}

```

## [Best Practices](best-practice.md)


## Show and Tell - Part One - 1930

AVCapture + Rectangle.

## Machine Learning - 2200

## Show and Tell - Part Two - 2510


### MNISTVision

Concepts to be covered
* Spin off requests from other requests
* Use Core Image for processing
* Use Core ML for machine learning
