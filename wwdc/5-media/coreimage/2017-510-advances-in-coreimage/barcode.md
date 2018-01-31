## Barcode - David - 3530


### CIBarcodeDescriptor Objects Contain

The errorCorrectedPayload of the barcode

Additional code-specific properties such as

Aztec’s layerCount

QRCode’s maskPattern

```swift
// Get a CIBarcodeDescriptor from AVFoundation.framework
class MyMetadataOutputObjectsDelegate: NSObject, AVCaptureMetadataOutputObjectsDelegate {

func metadataOutput(_ output:
didOutput metadataObjects: [
,
],
) {
if let
from connection:
mrc = metadataObjects. ?
descriptor = mrc. { (descriptor)
,

AVCaptureMetadataOutput
AVCaptureConnection
AVMetadataObject
first
as
AVMetadataMachineReadableCodeObject
descriptor
} }
}
```

#### Vision

code

#### CoreImage

code

### Demo: Detection and Re-Generation of a QRCode
