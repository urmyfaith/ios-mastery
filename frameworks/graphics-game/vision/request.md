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


## [`VNTargetedImageRequest`](https://developer.apple.com/documentation/vision/vntargetedimagerequest)


init(targetedCGImage: CGImage, options: [VNImageOption : Any] = [:])

init(targetedCGImage: CGImage, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedCGImage: CGImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(targetedCGImage: CGImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedCIImage: CIImage, options: [VNImageOption : Any] = [:])

init(targetedCIImage: CIImage, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedCIImage: CIImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(targetedCIImage: CIImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedCVPixelBuffer: CVPixelBuffer, options: [VNImageOption : Any] = [:])

init(targetedCVPixelBuffer: CVPixelBuffer, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedCVPixelBuffer: CVPixelBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(targetedCVPixelBuffer: CVPixelBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedImageData: Data, options: [VNImageOption : Any] = [:])

init(targetedImageData: Data, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedImageData: Data, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(targetedImageData: Data, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedImageURL: URL, options: [VNImageOption : Any] = [:])

init(targetedImageURL: URL, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)

init(targetedImageURL: URL, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:])

init(targetedImageURL: URL, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any] = [:], completionHandler: VNRequestCompletionHandler? = nil)
