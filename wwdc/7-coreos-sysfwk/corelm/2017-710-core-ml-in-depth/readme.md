
# [710 Core ML in depth](https://developer.apple.com/videos/play/wwdc2017/710/)

* Krishna Sridhar, Core ML
* Zach Nation, Core ML

## This Session

* Use cases
* Hardware optimized
* Obtaining models


Development Flow

```swift
let model = FlowerClassifier()
if let prediction = try? model.prediction(image: image) { return prediction.flowerType
}
```

## Use cases

* Sentiment Analysis
* Personalization
* Gesture Recognition
* Style Transfer
* Object Detection
* Music Tagging
* Summarization

## Models as Functions

Value Type | Data Type
--|--
Numeric | Double, Int64
Categories | String, Int64
Images | [CVPixelBuffer](https://developer.apple.com/documentation/corevideo/cvpixelbuffer-q2e)
Arrays |  [MLMultiArray](https://developer.apple.com/documentation/coreml/mlmultiarray)
Dictionaries | [String : Double], [Int64 : Double]


## Working with Text

### Using Other Formats

Word Counts

### Making Predictions


### Language Models


### Shakespeare Keyboard

## Hardware Optimized


### Demo Summary

```python
import coremltools
caffe_model = ('flowers.caffemodel','flowers.prototxt')
model = coremltools.converters.caffe.convert(
caffe_model, image_input_names = 'data', class_labels = 'labels.txt')
model.save('FlowerClassifier.mlmodel')
```
