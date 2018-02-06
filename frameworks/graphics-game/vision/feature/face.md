# Face




## [`VNDetectFaceRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetectfacerectanglesrequest)

(No contents)

## [`VNDetectFaceLandmarksRequest`](https://developer.apple.com/documentation/vision/vndetectfacelandmarksrequest)

(No contents)


### [`VNFaceObservationAccepting`](https://developer.apple.com/documentation/vision/vnfaceobservationaccepting)

var inputFaceObservations: [VNFaceObservation]? { get set }




## [`VNFaceObservation`](https://developer.apple.com/documentation/vision/vnfaceobservation)


## Landmark and Region

x|Landmark | Region
--|--|--
abstract| [`VNFaceLandmarks`](https://developer.apple.com/documentation/vision/vnfacelandmarks) |[`VNFaceLandmarkRegion`](https://developer.apple.com/documentation/vision/vnfacelandmarkregion)
2D|[`VNFaceLandmarks2D`](https://developer.apple.com/documentation/vision/vnfacelandmarks2d) | [`VNFaceLandmarkRegion2D`](https://developer.apple.com/documentation/vision/vnfacelandmarkregion2d)

### [`VNFaceLandmarks`](https://developer.apple.com/documentation/vision/vnfacelandmarks)



### [`VNFaceLandmarks2D`](https://developer.apple.com/documentation/vision/vnfacelandmarks2d)

var allPoints: VNFaceLandmarkRegion2D? { get }

```
var faceContour: VNFaceLandmarkRegion2D?
var innerLips: VNFaceLandmarkRegion2D?
var leftEye: VNFaceLandmarkRegion2D?
var leftEyebrow: VNFaceLandmarkRegion2D?
var leftPupil: VNFaceLandmarkRegion2D?
var medianLine: VNFaceLandmarkRegion2D?
var nose: VNFaceLandmarkRegion2D?
var noseCrest: VNFaceLandmarkRegion2D?
var outerLips: VNFaceLandmarkRegion2D?
var rightEye: VNFaceLandmarkRegion2D?
var rightEyebrow: VNFaceLandmarkRegion2D?
var rightPupil: VNFaceLandmarkRegion2D?
```

### [`VNFaceLandmarkRegion`](https://developer.apple.com/documentation/vision/vnfacelandmarkregion)

var pointCount: Int { get }

### [`VNFaceLandmarkRegion2D`](https://developer.apple.com/documentation/vision/vnfacelandmarkregion2d) : [`VNFaceLandmarkRegion`](https://developer.apple.com/documentation/vision/vnfacelandmarkregion)


\@nonobjc var normalizedPoints: [CGPoint] { get }


\@nonobjc func pointsInImage(imageSize: CGSize) -> [CGPoint]
