

[`VNDetectRectanglesRequest`](https://developer.apple.com/documentation/vision/vndetectrectanglesrequest)


var maximumObservations: Int { get set }

var minimumSize: Float { get set }

var minimumAspectRatio: VNAspectRatio { get set }

var maximumAspectRatio: VNAspectRatio { get set }

var minimumConfidence: VNConfidence { get set }

var quadratureTolerance: VNDegrees { get set }


typealias VNConfidence = Float

typealias VNAspectRatio = Float

typealias VNDegrees = Float



## [`VNRectangleObservation`](https://developer.apple.com/documentation/vision/vnrectangleobservation)


var bottomLeft: CGPoint { get }
