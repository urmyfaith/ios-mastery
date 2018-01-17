# observation.md


* NSObject
  * [`VNObservation`](https://developer.apple.com/documentation/vision/vnobservation)
    * [`VNDetectedObjectObservation`](https://developer.apple.com/documentation/vision/vndetectedobjectobservation)
      * [`VNFaceObservation`](https://developer.apple.com/documentation/vision/vnfaceobservation)
      * [`VNRectangleObservation`](https://developer.apple.com/documentation/vision/vnrectangleobservation)
        * [`VNBarcodeObservation`](https://developer.apple.com/documentation/vision/vnbarcodeobservation)
      * [`VNTextObservation`](https://developer.apple.com/documentation/vision/vntextobservation)
    * [`VNClassificationObservation`](https://developer.apple.com/documentation/vision/vnclassificationobservation)
    * [`VNPixelBufferObservation`](https://developer.apple.com/documentation/vision/vnpixelbufferobservation)
    * [`VNCoreMLFeatureValueObservation`](https://developer.apple.com/documentation/vision/vncoremlfeaturevalueobservation)
    * [`VNImageAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagealignmentobservation)
      * [`VNImageHomographicAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagehomographicalignmentobservation)
      * [`VNImageTranslationAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagetranslationalignmentobservation)
    * [`VNHorizonObservation`](https://developer.apple.com/documentation/vision/vnhorizonobservation)


## [`VNObservation`](https://developer.apple.com/documentation/vision/vnobservation)

var confidence: VNConfidence { get }

typealias VNConfidence = Float

var uuid: UUID { get }
