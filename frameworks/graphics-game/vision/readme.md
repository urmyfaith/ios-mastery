
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
Face Detection and Recognition |  VNDetectFaceRectanglesRequest <br/> VNDetectFaceLandmarksRequest |  VNFaceObservation
Machine Learning Image Analysis |  VNCoreMLRequest |  VNClassificationObservation <br/>  VNPixelBufferObservation <br/>  VNCoreMLFeatureValueObservation
Barcode Detection |  VNDetectBarcodesRequest |  VNBarcodeObservation
Image Alignment Analysis |  VNImageRegistrationRequest <br/> <br/> VNHomographicImageRegistrationRequest <br/> VNTranslationalImageRegistrationRequest |  VNImageAlignmentObservation <br/> VNImageHomographicAlignmentObservation <br/> VNImageTranslationAlignmentObservation
Text Detection |  VNDetectTextRectanglesRequest |  VNTextObservation
Horizon Detection |  VNDetectHorizonRequest |  VNHorizonObservation
Object Detection and Tracking |  VNDetectRectanglesRequest <br/> VNTrackRectangleRequest <br/> VNTrackObjectRequest | - <br/> VNRectangleObservation <br/> VNDetectedObjectObservation
