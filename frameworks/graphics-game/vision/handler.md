


[`VNImageRequestHandler`](https://developer.apple.com/documentation/vision/vnimagerequesthandler)

Initializers
init(cgImage: CGImage, options: [VNImageOption : Any] = [:])

init(cgImage: CGImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(ciImage: CIImage, options: [VNImageOption : Any] = [:])

init(ciImage: CIImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(cvPixelBuffer: CVPixelBuffer, options: [VNImageOption : Any] = [:])

init(cvPixelBuffer: CVPixelBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(data: Data, options: [VNImageOption : Any] = [:])

init(data: Data, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(url: URL, options: [VNImageOption : Any] = [:])

init(url: URL, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])


### func perform([VNRequest])

### example

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



## [`VNSequenceRequestHandler`](https://developer.apple.com/documentation/vision/vnsequencerequesthandler)


func perform([VNRequest], on: CGImage)

func perform([VNRequest], on: CIImage)

func perform([VNRequest], on: CVPixelBuffer)

func perform([VNRequest], on: CGImage, orientation: CGImagePropertyOrientation)

func perform([VNRequest], on: CIImage, orientation: CGImagePropertyOrientation)

func perform([VNRequest], on: CVPixelBuffer, orientation: CGImagePropertyOrientation)

func perform([VNRequest], onImageData: Data)

func perform([VNRequest], onImageData: Data, orientation: CGImagePropertyOrientation)

func perform([VNRequest], onImageURL: URL)

func perform([VNRequest], onImageURL: URL, orientation: CGImagePropertyOrientation)


### Example


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
