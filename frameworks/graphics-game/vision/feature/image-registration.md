

## Request

*
  * [`VNImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vnimageregistrationrequest)
    * [`VNTranslationalImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vntranslationalimageregistrationrequest)
    * [`VNHomographicImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vnhomographicimageregistrationrequest)


## [`VNImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vnimageregistrationrequest)

(no contents)


## [`VNTranslationalImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vntranslationalimageregistrationrequest)

(no contents)

## [`VNHomographicImageRegistrationRequest`](https://developer.apple.com/documentation/vision/vnhomographicimageregistrationrequest)

(no contents)


## Observation


* [`VNImageAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagealignmentobservation)
  * [`VNImageHomographicAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagehomographicalignmentobservation)
  * [`VNImageTranslationAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagetranslationalignmentobservation)


### [`VNImageAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagealignmentobservation)


### [`VNImageHomographicAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagehomographicalignmentobservation)

Perspective warp information produced by an image alignment request.

var warpTransform: matrix_float3x3 { get set }


### [`VNImageTranslationAlignmentObservation`](https://developer.apple.com/documentation/vision/vnimagetranslationalignmentobservation)


Affine transform information produced by an image alignment request.

var alignmentTransform: CGAffineTransform { get set }
