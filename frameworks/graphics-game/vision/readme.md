
# [Vision](https://developer.apple.com/documentation/vision)


## WWDC

* 2017
  * [506 Vision Framework: Building on Core ML](https://developer.apple.com/videos/play/wwdc2017/506/) // [Note]()


## Overview

* handlers
* requests
* [observations](observation.md)


## By Features

Feature | Request | Observation
--|--|--
[Face Detection and Recognition](feature/face.md) |  VNDetectFaceRectanglesRequest <br/> VNDetectFaceLandmarksRequest |  VNFaceObservation
[Machine Learning Image Analysis](feature/coreml.md) |  VNCoreMLRequest |  VNClassificationObservation <br/>  VNPixelBufferObservation <br/>  VNCoreMLFeatureValueObservation
[Barcode Detection](feature/barcode.md) |  VNDetectBarcodesRequest |  VNBarcodeObservation
[Image Alignment Analysis](feature/image-registration.md) |  VNImageRegistrationRequest <br/> <br/> VNHomographicImageRegistrationRequest <br/> VNTranslationalImageRegistrationRequest |  VNImageAlignmentObservation <br/> VNImageHomographicAlignmentObservation <br/> VNImageTranslationAlignmentObservation
[Text Detection](feature/text.md) |  VNDetectTextRectanglesRequest |  VNTextObservation
[Horizon Detection](feature/horizon.md) |  VNDetectHorizonRequest |  VNHorizonObservation
Object Detection and Tracking |  VNDetectRectanglesRequest <br/> VNTrackRectangleRequest <br/> VNTrackObjectRequest | - <br/> VNRectangleObservation <br/> VNDetectedObjectObservation


[feature/rectangle.md](feature/rectangle.md)
