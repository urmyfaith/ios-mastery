



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

## Externals References.

###  [Part 2 – TextDetection as source for OCR](http://www.neurosurg.de/2017/10/17/part-2-textdetection-as-source-for-ocr/)


[DrNeuroSurg/OCRwithVisionAndCoreML-Part2](https://github.com/DrNeuroSurg/OCRwithVisionAndCoreML-Part2)
