# Vision Requests




* NSObject
  * [`VNRequest`](https://developer.apple.com/documentation/vision/vnrequest)
    * [`VNImageBasedRequest`](https://developer.apple.com/documentation/vision/vnimagebasedrequest)
      * [`VNDetectFaceRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetectfacerectanglesrequest)
      * [`VNDetectFaceLandmarksRequest`](https://developer.apple.com/documentation/vision/vndetectfacelandmarksrequest) - [`VNFaceObservationAccepting`](https://developer.apple.com/documentation/vision/vnfaceobservationaccepting)
      * [`VNCoreMLRequest`](https://developer.apple.com/documentation/vision/vncoremlrequest)
      * [`VNDetectBarcodesRequest`](https://developer.apple.com/documentation/vision/vndetectbarcodesrequest)
      * [`VNTargetedImageRequest`](https://developer.apple.com/documentation/vision/vntargetedimagerequest)
        * [`VNImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vnimageregistrationrequest)
          * [`VNTranslationalImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vntranslationalimageregistrationrequest)
          * [`VNHomographicImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vnhomographicimageregistrationrequest)
      * [`VNDetectRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetectrectanglesrequest)
      * [`VNTrackingRequest`](https://developer.apple.com/documentation/vision/vntrackingrequest)
        * [`VNTrackRectangleRequest`](https://developer.apple.com/documentation/vision/vntrackrectanglerequest)
      * [`VNDetectHorizonRequest`](https://developer.apple.com/documentation/vision/vndetecthorizonrequest)
      * [`VNDetectTextRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetecttextrectanglesrequest)

## [`VNRequest`](https://developer.apple.com/documentation/vision/vnrequest)

typealias VNRequestCompletionHandler = (VNRequest, Error?) -> Void

convenience init()

init(completionHandler: VNRequestCompletionHandler? = nil)

var completionHandler: VNRequestCompletionHandler? { get }

var preferBackgroundProcessing: Bool { get set }

var results: [Any]? { get }

var usesCPUOnly: Bool { get set }

## [`VNImageBasedRequest`](https://developer.apple.com/documentation/vision/vnimagebasedrequest)

var regionOfInterest: CGRect { get set }

## [`VNDetectFaceRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetectfacerectanglesrequest)

(No contents)

## [`VNDetectFaceLandmarksRequest`](https://developer.apple.com/documentation/vision/vndetectfacelandmarksrequest)

(No contents)


### [`VNFaceObservationAccepting`](https://developer.apple.com/documentation/vision/vnfaceobservationaccepting)

var inputFaceObservations: [VNFaceObservation]? { get set }
