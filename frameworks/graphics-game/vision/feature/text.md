


## [`VNDetectTextRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetecttextrectanglesrequest)


var reportCharacterBoxes: Bool { get set }


## [`VNTextObservation`](https://developer.apple.com/documentation/vision/vntextobservation) : [`VNDetectedObjectObservation`](https://developer.apple.com/documentation/vision/vndetectedobjectobservation)

var characterBoxes: [VNRectangleObservation]?

var boundingBox: CGRect { get } // inherited from VNDetectedObjectObservation

##

## Update on 18-131

Just realized that it only detect the bounds, not the text itself. :-(

https://stackoverflow.com/questions/44533148/converting-a-vision-vntextobservation-to-a-string
