



## [`VNCoreMLRequest`](https://developer.apple.com/documentation/vision/vncoremlrequest)

convenience init(model: VNCoreMLModel)

init(model: VNCoreMLModel,
completionHandler: VNRequestCompletionHandler? = nil)

var model: VNCoreMLModel { get }

var imageCropAndScaleOption: VNImageCropAndScaleOption { get set }


### [`VNCoreMLModel`](https://developer.apple.com/documentation/vision/vncoremlmodel)

convenience init(for model: MLModel) throws

### [`VNImageCropAndScaleOption`](https://developer.apple.com/documentation/vision/vnimagecropandscaleoption), enum

case | rawValue | meaning
--|--|--
centerCrop | 0 |
scaleFit | 1
scaleFill | 2


## [`VNClassificationObservation`](https://developer.apple.com/documentation/vision/vnclassificationobservation)

var identifier: String { get }
