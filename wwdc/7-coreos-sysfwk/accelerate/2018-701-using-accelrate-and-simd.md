# [2018 701 Using Accelerate and simd](https://developer.apple.com/videos/play/wwdc2018/701)

2018-701-using-accelrate-and-simd.md

Learn how to use sophisticated Signal and Image Processing techniques to bring higher performance to your apps while lowering battery consumption. See compelling use cases for the Accelerate framework with interactive demos. Explore using simd—a valuable addition that effortlessly brings vector programming to your apps.

3648


d 

x

- Matthew Badin, CoreOS, Vector and Numerics 
- Luke Chang, CoreOS, Vector and Numerics


- A ccelerate
- vDSP
- simd
- vImage


## x 

```swift 
vDSP—Signal processing
vImage—Image processing
vForce—Vector transcendental functions
BLAS, LAPACK, LinearAlgebra—Dense matrix computations Sparse BLAS, Sparse Solvers—Sparse matrix computations BNNS—Neural networks
```


## [vImage](2018-701-2-vimage.md)  | Luke Chang | 1930 


### Demo 2230


### Workflow 


- Receive captured image from camera
- Prepare vImage input/output buffers
- Apply effects with vImage functions
- Display output image on screen

Adjust Color Saturation

The formula to adjust color saturation is:

```
Cb = ((Cb - 128) * saturation) + 128 
Cr = ((Cr - 128) * saturation) + 128
```


 ```swift
var preBias: Int16 = -128
// Fixed-Point Arithmetics in Q12 Format
let divisor: Int32 = 0x1000
var postBias: Int32 = 128 * divisor
 
// Convert Saturation to Q12 Format
 var matrix = [ Int16(saturation * Float(divisor)) ]
 
vImageMatrixMultiply_Planar8(&sources, &destinations, 1, 1,
 &matrix, divisor, &preBias, &postBias,
 vImage_Flags(kvImageNoFlags))
```

 #### Receive captured image from camera


```swift 
// AVCaptureVideoDataOutputSampleBufferDelegate
func captureOutput(_ output: AVCaptureOutput,
didOutput sampleBuffer: CMSampleBuffer,
from connection: AVCaptureConnection) {

    // Get CVImageBuffer from CMSampleBuffer
    let pixelBuffer = sampleBuffer.imageBuffer
 
    // Make Sure pixelBuffer Is Accessible to CPU
    CVPixelBufferLockBaseAddress(pixelBuffer, .readOnly)
    // Apply Effects with vImage Functions
    ...
 
    // Unlock the BaseAddress of pixelBuffer
    CVPixelBufferUnlockBaseAddress(pixelBuffer, .readOnly)
}
```

